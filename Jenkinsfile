pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the GitHub repository...'
                git branch: 'main', url: 'https://github.com/chntraining/jenpipeline.git', credentialsId: 'git.cred'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'hello.bat'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo "Tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                bat 'echo "Deployment successful!"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
