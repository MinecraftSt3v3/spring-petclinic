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
                //sh 'curl -u admin:password123 -X PUT "172.17.0.2:8081/artifactory/libs-release/spring-petclinic-2.7.0.jar" -T /home/newuser'
            }
        }
    }
}
