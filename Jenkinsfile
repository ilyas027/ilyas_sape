pipeline{
	agent any
	
	stages {
		stage ('Compile stage'){
			steps {
				withMaven(maven : 'maven_3.5.4') {
					bat 'mvn clean compile'
				}
			}
		}
			
		stage ('Testing Stage'){
			steps { 
				withMaven(maven : 'maven_3.5.4'){
					bat 'mvn test'
				}
			}
			
		}
		
		stage ('Deployment stage') {
			steps {
				withMaven(maven : 'maven_3.5.4'){
					bat 'mvn deploy'
				}
			}
			
		}
	
	}
}
