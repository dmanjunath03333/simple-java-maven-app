pipeline {
   agent any
tools {
    maven 'SampleMaven'
    jdk 'JDK1.8'
  }
   stages {
      stage('BUILD') {
           steps {
           
           sh "mvn -B -DskipTests clean install"
         }
        }     
    stage('Snar Scan') {
           steps {           
           sh "mvn sonar:sonar \
               -Dsonar.projectKey=project \
               -Dsonar.host.url=http://13.71.118.170:9000 \
               -Dsonar.login=dd9ec1ed7ff71da76a89c0425fb21764e4425526"
         }
       }  
}

}
