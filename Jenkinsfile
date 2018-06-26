pipeline {
		agent any
		stages {
			stage('Build') {
				steps {
					bat 'mvn package'
										
				}
			}		
			stage('Test') {
				steps {
				        bat 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App'
				}
				post {
					always {
						archive "target/**/*"
						junit 'target/surefire-reports/*.xml'
					}
				}
			}
			stage('Deliver') { 
				steps {
					bat './jenkins/scripts/deliver.sh' 
				}
			}							
		}			
}	
