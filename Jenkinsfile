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
            sh "mvn clean package sonar:sonar"
		//'-Dsonar.projectKey=sonartest7 ' +
		//'-Dsonar.projectName=sonartest7 ' +
		//'-Dsonar.projectVersion=1.0 ' +
		//'-Dsonar.sources= $PWD/src/main/java/ ' +
		//Language
		//'-Dsonar.language=java ' +
		//'-Dsonar.java.binaries=./target/classes ' +
		//Encoding of the source files
		//'-Dsonar.sourceEncoding=UTF-8'
        }
        
    }
}

  }
}
