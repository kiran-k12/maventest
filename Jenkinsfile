pipeline{
	agent any
	
stages{
	
	stage('SonarQube analysis') {
      steps {
        
           withMaven(maven : 'maven_3_5_0') {
        withSonarQubeEnv('sonar') {
          bat 'mvn clean package sonar:sonar'
        }
      }
    }
           }
	
}
}

