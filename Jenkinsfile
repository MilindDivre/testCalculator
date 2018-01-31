pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
					echo "hello"
					bat 'start cmd.exe /K mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven') {
					bat 'start cmd.exe /K mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Maven') {
					bat 'start cmd.exe /K mvn deploy'
                }
            }
        }
    }
}