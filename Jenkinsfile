pipeline {
    agent any

    tools {
        maven 'M2_HOME'
    }

    environment {
        APP_ENV = "DEV"
    }

    stages {

        stage('Code Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/Mayarahachani/mayara_hachani-TWIN8.git',
                    credentialsId: 'jenkins-example-github-pat'
            }
        }

        stage('Code Build') {
            steps {
                // Si le pom.xml est dans un sous-dossier, mettre le nom du dossier
                // dir('atelier-jenkins') {
                    sh 'mvn clean compile'
                // }
            }
        }

    }

    post {
        always {
            echo "======always======"
        }
        success {
            echo "=====pipeline executed successfully ====="
        }
        failure {
            echo "======pipeline execution failed======"
        }
    }
}
