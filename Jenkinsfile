pipeline {
    agent any

    // Parameters for the build
    parameters {
        booleanParam(
            name: 'executeTests',
            defaultValue: true,
            description: 'Run Test stage?'
        )
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
                // Your build commands here
            }
        }

        stage('Test') {
            when {
                // Test stage runs only if executeTests is true
                expression { params.executeTests }
            }
            steps {
                echo "Testing only because executeTests = true"
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
