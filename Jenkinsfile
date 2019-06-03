pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'C:\\personal_projects\\apache-maven-3.6.1-bin\\apache-maven-3.6.1\\bin\\mvn -B -DskipTests clean package'
            }
        }
    }
}
