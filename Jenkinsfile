pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/ksks0000/Jenkins-learning.git'
        GIT_BRANCH = 'dev'
        SSH_KEY = credentials('2100fc81-e2fe-426d-a0b8-ff04b37c45b7')  
    }
    
    stages {
        stage('Checkout from SCM'){ 
            steps {
                // u slucaju  da je public repo moze bez credentialsId
                // git branch: 'dev', url: 'https://github.com/ksks0000/Jenkins-learning.git'
                // za private repo:  //da vidimo dal ce ovako da radi
                git(
                    url: "${GIT_REPO_URL}",
                    branch: "${GIT_BRANCH}",
                    credentialsId: "${SSH_KEY}", 
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
                // Install Composer dependencies (e.g., for a Drupal project)
                //sh 'composer install --no-interaction --prefer-dist'
            }
        } 
        stage ('Test') {
              steps {
                echo "Testing ..."
                sh '''
                echo " test tasks "
                '''
                // Example for running PHPUnit tests (adjust if using another testing framework)
                //sh './vendor/bin/phpunit --configuration phpunit.xml'
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
