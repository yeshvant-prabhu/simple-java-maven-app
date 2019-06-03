pipeline {
    agent{
        docker{
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
   }
   options{
      skipStagesAfterUnstable()
   }
    stages {
        stage('Build') {
            steps {
                bat 'C:\\personal_projects\\apache-maven-3.6.1-bin\\apache-maven-3.6.1\\bin\\mvn -B -DskipTests clean package'
            }
        }
    }
}
