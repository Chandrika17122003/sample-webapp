pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Code fetched from GitHub'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                echo 'Deploying application to Nginx'

                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl reload nginx
                '''
            }
        }
    }
}

