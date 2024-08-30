pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                // Replace with your actual build steps
                sh 'echo "Building the project..."'
            }
        }

        stage('Test') {
            steps {
                // Replace with your test commands
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') {
            steps {
                // Replace with your deployment steps
                sh 'echo "Deploying the application..."'
            }
        }
    }

    post {
        success {
            // Send success email
            emailext(
                subject: "SUCCESS: Build ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "Good news! The build was successful.\n\n${env.BUILD_URL}",
                to: 'kishorekannandevops@gmail.com'
            )
        }
        failure {
            // Send failure email
            emailext(
                subject: "FAILURE: Build ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "Unfortunately, the build failed.\n\n${env.BUILD_URL}",
                to: 'kishorekannandevops@gmail.com'
            )
        }
    }
}
    }
}
