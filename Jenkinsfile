pipeline {

    agent any

    stages {

        stage('Build Maven') {

            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {

            steps {
                sh 'docker build -t java-app .'
            }
        }

        stage('Remove Old Container') {

            steps {
                sh 'docker rm -f java-container || true'
            }
        }

        stage('Run Docker Container') {

            steps {
                sh 'docker run -d --name java-container java-app'
            }
        }
    }
}
