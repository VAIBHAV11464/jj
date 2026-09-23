pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/VAIBHAV11464/jj.git'
            }
        }
        stage('Show Build Info') {
            steps {
                echo "Build Number: ${env.BUILD_NUMBER}"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Workspace: ${env.WORKSPACE}"
            }
        }
        stage('Run Linter') {
            steps {
                bat 'python -m flake8 app.py'
            }
        }
    }
}