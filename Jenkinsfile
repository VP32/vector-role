pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', credentialsId: '0f8923e7-fb7a-458c-942a-502970857c50', url: 'https://github.com/VP32/vector-role'
            }
        }
        stage('Install required') {
            steps{
                sh 'pip3 install molecule molecule_docker'
            }
        }
        stage('Run molecule test') {
            steps{
                sh 'molecule test'
            }
        }
    }
}
