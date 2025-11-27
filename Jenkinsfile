pipeline {
    agent any

    stages {
        stage('Secure API Call') {
            steps {
                script {
                    withCredentials([string(credentialsId: 'GITHUB_TOKEN', variable: 'GH_TOKEN')]) {
                        sh '''
                            echo "Calling GitHub API securely..."
                            curl -H "Authorization: Bearer $GH_TOKEN" https://api.github.com/user
                        '''
                    }
                }
            }
        }
    }
}
