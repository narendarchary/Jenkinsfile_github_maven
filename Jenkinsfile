pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Git Clone') {
            steps {
            }    
            }
		stage('Maven Version'){
			steps{
				sh 'mvn version'
			}
			}
		stage('Maveen Clean'){
			steps{
				sh 'mvn clean'
			}
			}
		stage('Maven Validate'){
			steps{
				sh 'mvn validate'
			}
			}
		stage('Maven Compile'){
			steps{
				sh 'mvn compile'
			}
			}
		stage('Maven Package'){
			steps{
				sh 'mvn package'
			}
			}
			
            
            
        }
    }

