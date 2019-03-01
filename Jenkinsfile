pipeline {
agent any
  tools {
   maven 'maven3.6.0'
    jdk 'java1.8.0'
  }
  
  stages {
    stage('Build') {
          steps {
            sh "mvn -B -DskipTests clean package"
          }
          }
       
    stages {
      stage ('Deploy') {
        sh "java -jar target/my-app-1.0-SNAPSHOT.jar"
      }
    }
          
          
  }

}
