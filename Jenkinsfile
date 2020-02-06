pipeline{
	agent any
	tools { 
        maven 'maven_3_5_0' 
    }

stages{
	
      stage('Sonarqube') {
    environment {
        scannerHome = tool 'SONAR_RUNNER_4.2'
    }
    steps {
        withSonarQubeEnv('sonar') {
            sh "/home/divyasekaran94/sonar-scanner/bin/sonar-scanner"
        }
        
    }
}

  }
}
