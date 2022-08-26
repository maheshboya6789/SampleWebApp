pipeline {
    agent any

    stages {
        stage('GitHub Repo') {
            steps {
                git 'https://github.com/maheshboya6789/SampleWebApp.git'
            }
        }
        
        stage('Maven Build') {
            steps {
                sh "mvn clean install"
            }
        }
        
         stage('Deploy to Tomcat server') {
            steps {
              sshagent(['tomcat-user']) {
                
                   sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/pipeline_demo/target" ubuntu@35.81.169.188:/opt/tomcat/webapps" 
               }
            }
        }
    }
}
