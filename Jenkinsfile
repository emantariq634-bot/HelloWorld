pipeline {
    agent any

    // Environment Variables (custom)
    environment {
        APP_NAME    = "MySampleApp"
        APP_VERSION = "1.0.0"
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${APP_NAME} version ${APP_VERSION}..."
                // Your build commands here
            }
        }

        stage('Test') {
            when {
                expression { return true }   // change this condition when needed
            }
            steps {
                echo "Testing ${APP_NAME} version ${APP_VERSION} (condition is true)..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME} version ${APP_VERSION}..."
                // Your deploy commands here
            }
        }
    }

    post {
        always {
            echo "Build completed for ${APP_NAME} version ${APP_VERSION}! (Post section ran.)"
        }
    }
}
