pipeline {
    agent any  // Runs on any available Jenkins node

    stages {
        stage('Checkout') {
            steps {
                script {
                    echo "Checking out the branch: ${env.BRANCH_NAME}"
                }
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building the project on branch: ${env.BRANCH_NAME}"
                sh 'echo Build process started'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests on branch: ${env.BRANCH_NAME}"
                sh 'echo Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application from branch: ${env.BRANCH_NAME}"
                sh 'echo Deploying to environment'
            }
        }
    }
}
