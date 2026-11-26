pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                echo 'Getting application source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to Nginx'

                sh '''
                    sudo cp index.html /var/www/html/index.html
                '''
            }
        }
    }

    post {
        success {
            echo 'Application deployed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
