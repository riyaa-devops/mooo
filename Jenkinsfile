pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps { git 'YOUR_GITHUB_REPO_URL' }
        }
        stage('Build Maven Project') {
            steps { sh 'mvn clean package' }
        }
        stage('Build Docker Image') {
            steps { sh 'docker build -t java-maven-app .' }
        }
        stage('Run Docker Container') {
            steps { sh 'docker run java-maven-app' }
        }
    }
}
