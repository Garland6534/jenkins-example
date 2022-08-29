pipeline {
    agent any
    triggers {
        cron('H/5 * * * *')
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven() {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven() {
                    sh 'mvn test'
                }
            }
        }

    }
}
