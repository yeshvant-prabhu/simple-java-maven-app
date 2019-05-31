pipeline{
  agent{
    docker{
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
     }
   }
   options{
      skipStagesAfterUnstable()
   }
   stages{
      stage('Build'){
          steps {
              bat 'mvn -B -DskipTests clean package'
          }
          post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') { 
            steps {
                bat './jenkins/scripts/deliver.sh' 
            }
        }
   }
}
