pipeline {
    agent any

    tools {
        maven 'maven3.8'
        jdk 'jdk21'
    }

    stages {
        stage('Compilar') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Empaquetar') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

