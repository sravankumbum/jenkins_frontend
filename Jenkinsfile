pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/sravankumbum/jenkins_frontend'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Start Frontend') {
            steps {
                sh 'pm2 restart frontend || pm2 start npm --name frontend -- start'
            }
        }
    }
}
