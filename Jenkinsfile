pipeline {
    agent any

    stages {
        stage('Pull Source Code') {
            steps {
            git branch: 'main', url: 'https://github.com/richieze/e-voting-app.git'
            }
        }
    stage('Build Container Image') {
        steps {
            sh 'docker compose build'
            }
        }
    stage('Deploy Container Apps') {
        steps {
            sh 'docker compose up -d'
            }
        }
    stage('Push Image Apps') {
        steps {
            sh 'docker compose push'
            }
        }
    }
}
