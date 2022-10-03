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

            sh 'curl https://github.com/MinecraftSt3v3/spring-petclinic/blob/main/Jenkinsfile'
            }
        }
        }
    }
