pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw package'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'curl -u admin:password123 -X PUT "172.17.0.2:8081/artifactory/spring-clinic/spring-petclinic-2.7.0-SNAPSHOT.jar" -T "/home/alpuser/.jenkins/workspace/maven/target/spring-petclinic-2.7.0-SNAPSHOT.jar"'
            }
        }
    }
