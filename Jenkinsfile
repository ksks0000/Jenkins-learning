pipeline {
    agent any
    stages {
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
                echo " deliver tasks "
                '''
            }
        } 
    }
}
