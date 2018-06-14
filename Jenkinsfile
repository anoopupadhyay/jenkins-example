pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
              
                    sh 'mvn clean compile package'
                
            }
        }

        stage ('Testing Stage') {

            steps {
               
                    sh 'mvn test'
                
            }
        }
 stage (' Test') {
            steps {
               
                    build job: 'static analysis'
                
            }
        }

        stage ('Deployment Stage') {
            steps {
               
                    build job: 'Deploy-to-staging'
                
            }
        }
        stage ('Deployment Prod') {
            steps {
               
                    build job: 'Deploy-to-Prod'
                
            }
        }
    }
}
