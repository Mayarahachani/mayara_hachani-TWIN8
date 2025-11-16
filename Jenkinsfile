pipeline {
    agent any

    stages {
        stage('Initialisation') {
            steps {
                echo "Début du pipeline à partir du Jenkinsfile"
            }
        }

        stage('Récupération du code') {
            steps {
                git url: 'https://github.com/Mayarahachani/mayara_hachani-TWIN8.git'
            }
        }

        stage('Build Maven') {
            steps {
                sh 'mvn -v'
                sh 'mvn clean install'
            }
        }
    }
}
