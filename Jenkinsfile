pipeline {
		agent any
		stages {
			stage('Build') {
				steps {
					sh 'mvn package'
										
				}
			}		
			stage('Test') {
				steps {
				        sh 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App'
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
					sh './jenkins/scripts/deliver.sh' 
				}
			}							
		}			
}	
