
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Compile') {
            steps {
                bat 'python -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m unittest test_app.py'
            }
        }

        stage('Package') {
            steps {
                bat 'tar -czf app.tar.gz app.py'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }
        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}

