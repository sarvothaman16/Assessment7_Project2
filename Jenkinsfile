pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sarvothaman16/Assessment7_Project2.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat '"C:\\Users\\Sarvothaman R J\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt',
                              fingerprint: true
            }
        }
    }
}
