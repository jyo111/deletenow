pipeline {
    agent any
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn------'
                nodejs('nodejs') {
                    sh 'yarn install'
                }
            }
        }
        stage('run backend') {
            steps {
                echo 'executing Gradle---'
                withGradle() {
                    sh './gradlew -v'
                }
            }
        }
    }
}
