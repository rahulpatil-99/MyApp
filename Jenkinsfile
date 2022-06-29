pipeline {
    agent {
        docker { image 'node:16.13.1-alpine' }
    } 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo 'installing packages......'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing....'
                sh 'npm test'
            }
        }
        stage('Build app') {
            steps {
                echo 'Building app....'
                sh 'npm build-android'
            }
        }
    }
}