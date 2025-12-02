pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
    }

    post {
        success {
            echo "Build SUCCESS for ${env.GIT_COMMIT}"
        }
        failure {
            echo "Build FAILED for ${env.GIT_COMMIT}"
        }
    }
}
