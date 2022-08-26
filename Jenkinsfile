pipeline {
    agent any

    stages {
        stage('GitHub Repo') {
            steps {
                git 'https://github.com/maheshboya6789/SampleWebApp'
            }
        }
        
        stage('Maven Build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
