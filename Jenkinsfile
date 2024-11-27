pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/ksks0000/Jenkins-learning.git'
        GIT_BRANCH = 'dev'
    }
    
    stages {
        
        stage('Checkout from SCM'){ 
            steps {
                // u slucaju  da je public repo moze bez credentialsId
                // git branch: 'dev', url: 'https://github.com/ksks0000/Jenkins-learning.git'
                // za private repo:
                git(
                    url: "https://github.com/ksks0000/Jenkins-learning.git",
                    branch: "dev",
                    credentialsId: "2100fc81-e2fe-426d-a0b8-ff04b37c45b7", 
                    changelog: true,
                    poll: true
                )
            }      
        }
        
        stage ('Build') {
            steps {
                echo "Building ..."
                sh '''
                echo " build tasks "
                '''
            }
        } 
        stage ('Test') {
              steps {
                echo "Testing ..."
                sh '''
                echo " test tasks "
                '''
            }
        } 
        stage ('Deploy') {
              steps {
                echo "Deploying ..."
                sh '''
                echo " deploy tasks "
                '''
            }
        } 
    }
}
