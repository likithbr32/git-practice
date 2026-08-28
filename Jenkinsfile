pipeline {
    agent any

    environment {
        APP_NAME = 'git-practice'
        APP_ENV = 'dev'
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${APP_NAME}"
                echo "Environment: ${APP_ENV}"
                sh 'echo Build completed'
            }
        }

        stage('Test') {
            steps {
                echo "Testing ${APP_NAME}"
                sh 'echo Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME}"
                echo "Environment: ${APP_ENV}"
                sh 'echo Deployment completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }

        always {
            echo 'Pipeline finished.'
        }
    }
}
