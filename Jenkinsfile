pipeline {
    agent any

    tools {
        maven 'Maven_3.8.7'
        jdk 'JDK_21'
    }

    stages {
        stage('Clonar Repo') {
            steps {
                git 'https://github.com/JpHernandezOrellana/saludoapp.git'
            }
        }

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
    }

    post {
        success {
            echo '¡Compilación y pruebas completadas con éxito!'
        }
        failure {
            echo 'La compilación o pruebas fallaron.'
        }
    }
}

