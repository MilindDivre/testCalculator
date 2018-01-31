pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
					echo "hello"
					bat 'start mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven') {
					bat 'start mvn test'
					writeFile file: '.archive-jenkins-maven-event-spy-logs', text: ''
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Maven') {
					bat 'start cmd.exe mvn install'
                }
            }
        }
    }
}