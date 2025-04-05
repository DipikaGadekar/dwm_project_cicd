pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/DipikaGadekar/dwm_project_cicd.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t dwm_project_image .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 dwm_project_image'
            }
        }
    }
}
