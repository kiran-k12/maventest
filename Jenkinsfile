pipeline{
	agent any
	
stages{
	stage ('Compile') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
              //      sh 'mvn clean package'
                    bat 'mvn clean compile'
                }
            }
        }
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

