pipeline {
    agent any
    environment {
    ARTI_CRED_ID = credentials('arti-cred-id')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
        echo env.BRANCH_NAME
        sh "./mvnw package"
            }
        }
        stage('Deploy') {
        when {
        expression {
           env.BRANCH_NAME == 'main'
        }
        }
            steps {
                echo 'Deploying....'
  usernameVariable: 'user')]) {
            sh 'curl -u ${user}:${pw} -X PUT "172.17.0.3:8081/artifactory/libs-release/spring-petclinic-2.7.0.jar" -T /home/alpuser/.jenkins/workspace/jenkins-pipeline_main/target/spring-petclinic-2.7.0.jar'
            }
        }
        }
    }
}
