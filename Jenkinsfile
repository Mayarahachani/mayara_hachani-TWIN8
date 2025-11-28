pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }

        stage('Tests') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    }
}
