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
      
}

}
