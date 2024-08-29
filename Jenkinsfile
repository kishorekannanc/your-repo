pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo "Building spr the project..."'
                
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying the project..."'
                
            }
        }
    }

    post {
        success {
            mail to: 'kishorekannandevops@gmail.com',
                 subject: "Build Successful: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "The build was successful!\n\nCheck it here: ${env.BUILD_URL}"
        }
        failure {
            mail to: 'kishorekannandevops@gmail.com',
                 subject: "Build Failed: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "The build failed!\n\nCheck it here: ${env.BUILD_URL}"
        }
    }
}
