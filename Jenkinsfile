pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/hellabond/python-ci-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Use Windows batch command
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Run Python unit tests
                bat 'python -m unittest discover'
            }
        }
    }
}
