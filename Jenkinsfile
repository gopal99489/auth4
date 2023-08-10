pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'cd auth4 && npm install && npm run build'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sh 'sudo /var/www/html/*
                sh 'sudo docker container run -dt --name dist -p 8083:80 --volume /home/ubuntu/dist:/var/www/html'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Your application is built and ready for deployment.'
        }
        failure {
            echo 'Pipeline failed. Please check the logs and address any issues.'
        }
    }
}
