pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/dimpledimpu50-cmyk/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
