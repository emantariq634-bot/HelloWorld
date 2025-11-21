pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
                // Your build commands here
            }
        }

        stage('Test') {
            when {
                expression { return true }   // change this condition when needed
            }
            steps {
                echo "Testing only when condition is true"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Your deploy commands here
            }
        }
    }

    post {
        always {
            echo 'Build completed! (Post section ran.)'
        }
    }
}
