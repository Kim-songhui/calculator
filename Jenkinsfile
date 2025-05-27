pipeline {
    agent any

    tools {
        gradle 'Gradle'  // Jenkins에 등록한 도구 이름과 일치해야 함
    }

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'ee01eab3ee4540b08042a5eeb76f45e0', url: 'https://github.com/Kim-songhui/calculator.git'
            }
        }

        stage('Build and Test') {
            steps {
                sh './gradlew clean build test'
            }
        }
    }
}