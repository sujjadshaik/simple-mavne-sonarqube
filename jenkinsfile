pipeline{
   agent any;
   tools{
       maven 'maven'
       jdk 'JDK11'
   }
  stages {
          stage("build & SonarQube analysis") {
            agent any
            steps {
              withSonarQubeEnv('sonar-server-local') {
                sh 'java -version'
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
    }
}
