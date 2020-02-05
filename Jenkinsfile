pipeline{
	agent any
	tools { 
        maven 'maven_3_5_0' 
    }

stages{
	stage("Clear Environment"){
            steps{
                deleteDir()
                
            } 
         }
      stage('Build & Package') {
	      step{
    withSonarQubeEnv('sonar') {
        sh 'mvn clean package sonar:sonar'
    }
   }
}


  }
}
