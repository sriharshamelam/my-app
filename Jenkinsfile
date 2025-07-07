pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                script {
                    git branch: 'main', changelog: false, poll: false, url: 'https://github.com/sriharshamelam/my-app.git'
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