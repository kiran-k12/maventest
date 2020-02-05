pipeline{
	tools { 
        maven 'maven_3_5_0' 
    }

stages{
	stage("Clear Environment"){
            steps{
                deleteDir()
                
            } 
         }
    stage ('Sonar scan'){
            steps {
        withSonarQubeEnv {
sonar.projectKey=sonartest6
sonar.projectName=sonartest6
sonar.projectVersion=1.0
sonar.sources= /var/lib/jenkins/workspace/sonartest/src/main/java/
# Language
sonar.language=java
sonar.java.binaries=./target/classes
# Encoding of the source files
sonar.sourceEncoding=UTF-8

sh 'mvn clean package'
}
 
        }
     }


  }
}
