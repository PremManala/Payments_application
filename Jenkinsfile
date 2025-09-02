
pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/yourusername/devops_portfolio_app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-portfolio-app .'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh './scripts/deploy.sh'
            }
        }
    }
}
