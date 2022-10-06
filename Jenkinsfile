pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "hello Build stage"
                sh './mvnw package'
            }
        }
        
        stage('Deploy') {
            steps {
                echo "hello deploy stage"
                sh 'curl -u admin:password123 -XPUT "172.17.0.2:8081/artifactory/spring-clinic/spring-petclinic-2.7.0-SNAPSHOT.jar" -T "/home/newuser/.jenkins/workspace/maven/target/spring-petclinic-2.7.0-SNAPSHOT.jar"'
            }
        }
    }
}
