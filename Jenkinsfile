pipeline {
    agent any

    stages {
        stage('code cloning') {
            steps {
                git 'https://github.com/Eswar12345678/Fresh.git'
            }
        }
        stage('code Building') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('code deploying') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '54530047-2586-4cc9-8db3-eb60d4d15783', path: '', url: 'http://13.201.95.29:8080/')], contextPath: 'eswar123.war', war: '**/*.war'
                deploy adapters: [tomcat9(credentialsId: '98920ad4-4b67-457e-aae3-6bea5bac9fee', path: '', url: 'http://13.201.95.29:8080/')], contextPath: 'eswar12', war: '**/*.war'
            }
        }
    }
}
