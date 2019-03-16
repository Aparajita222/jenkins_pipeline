pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MavenLocal') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MavenLocal') {
                    sh 'mvn test'
                }
            }
        }
        
       stage ('Package Stage') {

            steps {
                withMaven(maven : 'MavenLocal') {
                    sh 'mvn package'
                }
            }
        }

       stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'MavenLocal') {
                    sh 'mvn install'
                }
            }
        }
    }
}
