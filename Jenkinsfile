pipeline {
  
  agent any
  
  stages {
      
    stage("build") {
      steps {
        withMaven (maven : 'maven_3_8_5') {
          sh 'mvn clean compile'
          }
        }
      }
    stage("test") {
      steps {
        withMaven (maven : 'maven_3_8_5') {
          sh 'mvn test'
        }
      }
    }
    stage("deploy") {
      steps {
        withMaven (maven : 'maven_3_8_5')  {
          sh 'mvn deploy' 
        }
      }
    }
  }
}  
