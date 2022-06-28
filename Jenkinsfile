pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            agent {
                docker { image 'node:16.13.1-alpine' }
            }
            steps {
                echo 'Testing....'
                sh 'node --version'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}