

pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                echo 'Getting application source code'
                checkout scm
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
