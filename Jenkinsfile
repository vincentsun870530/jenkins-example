pipeline {
    agent any
     tools {
        maven 'Maven_3.5.0'
    }
    stages {
         
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Compile Stage') {
            steps {
                    sh 'mvn clean compile' 
            }
        }

        stage ('Testing Stage') {
            steps {
                    sh 'mvn test'
            }
        }

        stage ('Deployment Stage') {
            steps {               
                    sh 'mvn deploy'                
            }
        }
    }
}