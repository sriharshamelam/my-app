pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')  // Poll every 15 minutes
    }

    stages {
        stage('checkout') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/sriharshamelam/my-app.git'
                }
            }
        }
        stage('build') {
            steps {
                script {
                    bat 'mvn clean package'
                }
            }
        }
    }
}
