pipeline {
    agent any
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