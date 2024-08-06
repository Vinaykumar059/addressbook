pipeline {
    agent any
    stages {
        stage('Build') {
        steps {
                git 'https://github.com/Vinaykumar059/addressbook.git'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
