pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Jenkins-sample-project', url: 'https://github.com/ramakrishna-m/Jenkins-example-python.git']])
            }
        }
        stage('Build') {
            steps {
            git branch: 'main', credentialsId: 'Jenkins-sample-project', url: 'https://github.com/ramakrishna-m/Jenkins-example-python.git'
            bat 'C:\\Users\\root\\AppData\\Local\\Programs\\Python\\Python311\\python.exe hello.py'
            }
        }
        stage('Test') {
            steps {
                echo 'Job is tested'
            }
        }
    }
}
