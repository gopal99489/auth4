pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'cd auth4 && npm install && npm run build'
            }
        }
