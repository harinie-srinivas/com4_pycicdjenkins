pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/USERNAME/REPOSITORY.git'
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
}