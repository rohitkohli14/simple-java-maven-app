pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Hello Shagun'
            }
        }
        stage('Test') {
            steps {
                echo 'Hello Shraddha'
            }
            post {
                always {
                    echo 'Hello Paul'
                }
            }
        }
        stage('Deliver') {
            steps {
                echo 'Bye Rohit'
            }
        }
    }
