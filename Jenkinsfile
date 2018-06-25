pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Hello PAUL'
            }
        }
        stage('Test') {
            steps {
                echo 'Hello SHAGUN'
            }
            post {
                always {
                    echo 'Hello SHRADDHA'
                }
            }
        }
        stage('Deliver') {
            steps {
                echo 'Bye ROHIT'
            }
        }
    }
}
