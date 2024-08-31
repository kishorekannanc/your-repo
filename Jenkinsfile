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
                // Intentional failure to trigger the failure email
                sh 'exit 1'
            }
        }
    }

    post {
        success {
            emailext(
                subject: "SUCCESS: Build ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "Good job! The build was successful.\n\n${env.BUILD_URL}",
                to: 'kishorekannan0905@gmail.com,kishorekannandevops@gmail.com'
            )
        }
        failure {
            emailext(
                subject: "FAILURE: Build ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "Unfortunately, the build failed. Please check the details and correct the issue.\n\n${env.BUILD_URL}",
                to: 'kishorekannandevops@gmail.com'
            )
        }
    }
}
