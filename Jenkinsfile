
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sanjai238/DevOps_CI_24BCS238.git'
            }
        }

        stage('Build') {
            steps {
                bat 'python --version'
                bat 'python -m py_compile src/app.py'
                echo 'Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m unittest discover -s tests -p "test_app.py" -v'
            }
        }

        stage('Result') {
            steps {
                echo 'Calculator CI pipeline completed successfully'
            }
        }
    }
}
