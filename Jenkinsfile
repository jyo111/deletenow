pipeline {
    agent any
    tools {
        gradle 'Gradle 6.6.1'
    }
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
                    sh './gradlew -v'                
            }
        }
    }
}
