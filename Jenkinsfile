pipeline {
    agent any
    tools {
        jdk 'jdk17'   // 위에서 지정한 이름과 동일해야 함
    }
    stages {
        stage("Build") {
            steps {
                sh "./gradlew build"
            }
        }
        stage("Unit test") {
            steps {
                sh "./gradlew test"
            }
        }
    }
}