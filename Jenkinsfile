pipeline {
    agent any

   // tools {
         //Install the Maven version configured as "M3" and add it to the path.
        //maven "M3"
    //}

    stages {
        stage('Git Clone') {
            steps {
				git credentialsId: 'git', url: 'https://github.com/narendarchary/login.git'
            }    
            }
		stage('Maven Version'){
			steps{
				sh 'mvn --version'
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
		stage('Sonar Scan'){
			steps{
				sh 'mvn sonar:sonar -Dsonar.host.url=http://34.122.241.2:9000 -Dsonar.login=deb537e895900d57e9213b0cd8f3558b5bdc09db'
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

