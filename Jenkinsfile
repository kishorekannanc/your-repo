pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh 'make build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                sh 'make test'
            }
        }
    }

}
