pipeline{
	agent any
	
stages{
	
	stage('SonarQube analysis') {
      steps {
        
           
        withSonarQubeEnv('sonar') {
          bat 'mvn clean package sonar:sonar'
        }
     
    }
           }
	
}
}

