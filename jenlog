pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                echo "Deploying the project..."
                sudo grep  4[0-9][0-9]  /var/log/apache2/access.log || true
                sudo grep  5[0-9][0-9]  /var/log/apache2/access.log || true
                '''
            }
        }
    }
}
