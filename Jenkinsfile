pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/ksks0000/Jenkins-learning.git'
        GIT_BRANCH = 'dev'
    }
    
    stages {
        
        stage('Checkout from SCM'){ //check out the code from git repo into the jenkins workspace 
            steps {
                git branch: 'dev', url: 'https://github.com/ksks0000/Jenkins-learning.git'
                /*
                git(
                    url: "${GIT_REPO_URL}",
                    branch: "${GIT_BRANCH}",
                    // credentialsId: "git", 
                    changelog: true,
                    poll: true
                )
                */
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
