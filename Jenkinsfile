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
                bat '''
                python -m pip install --upgrade pip
                python -m pip install flake8
                python -m flake8 app.py
                '''
            }
        }
    }
}