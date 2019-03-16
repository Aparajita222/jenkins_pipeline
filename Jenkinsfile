pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Local Maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Local Maven') {
                    sh 'mvn test'
                }
            }
        }
        
       stage ('Package Stage') {

            steps {
                withMaven(maven : 'Local Maven') {
                    sh 'mvn package'
                }
            }
        }

       stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Local Maven') {
                    sh 'mvn install'
                }
            }
        }
    }
}
