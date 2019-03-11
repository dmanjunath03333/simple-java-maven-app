pipeline {
   agent any
tools {
    maven 'maven'
    jdk 'jdk'
  }
   
   stages {
      stage('BUILD') {
           steps {
           
           sh "mvn -B -DskipTests clean install"
         }
        }   
      stage ('Sonar'){
         steps {
          script {
         sh 'mvn sonar:sonar \
           -Dsonar.projectKey=key \
          -Dsonar.host.url=http://34.220.234.199:9000 \
           -Dsonar.login=bd632327e7f0e7f4c4a1675c398c64fd732620e8'  
     
          }
         }
      }
      
      stage('Building image') {
          steps {
          script {
            dockerImage = docker.build registry + ":$BUILD_NUMBER"
                }
               }
          }
     
      }

   
   
}
