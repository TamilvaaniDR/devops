pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'day4',
                url: 'https://github.com/TamilvaaniDR/devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t day3-image .'
            }
        }

        stage('Remove Old Container') {
            steps {
                sh 'docker rm -f day3-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name day3-container day3-image'
            }
        }

    }
}
