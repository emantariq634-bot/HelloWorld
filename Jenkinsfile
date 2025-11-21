pipeline {
    agent any

    tools {
        maven 'Maven3'  // Name MUST match Tools name exactly
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat "mvn -v"
            }
        }

        stage('Test') {
            when {
                expression { return true }
            }
            steps {
                echo "Testing only when condition is true"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            echo 'Build completed! (Post section ran.)'
        }
    }
}
