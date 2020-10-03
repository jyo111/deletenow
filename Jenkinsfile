pipeline {
    agent any 
    parameters {
        choise(name: 'VERSION', choises: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }   
    stages {        
        stage('Build') {
            steps {
               echo 'Hi' 
            }
        }
        stage('Test') {  
            when {
                expression {
                    params.executeTests
                }
            }          
            steps {
                echo 'Hello'
            }
        }
        stage('Deploy') {
            steps {
                echo '-----How---'    
                echo "deploying version ${params.VERSION}"        
                                
            }
        }
    } 
}
