pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the GitHub repository...'
                git 'https://github.com/your-username/jenkins-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'chmod +x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
