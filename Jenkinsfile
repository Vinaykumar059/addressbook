pipeline {
    agent any
    stages {
        stage('Build') {
        steps {
                git 'https://github.com/Vinaykumar059/addressbook.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('Deploy') {
            steps {
                deploy adapters: [tomcat9(url: 'http://172.31.33.12:8080',
                            credentialsId: 'tomcat-tomcat')],
                        war: 'target/*.war',
                        contextPath: 'app1'
    }
}
