pipeline {
    agent any
    environment {
        ENVI = "dev"
    }
    stages{
        stage("testing"){
            steps {
                script {
                    sh """
                      echo " This is Testing stage"
                      echo "$ENVI"
                    """
                }
            }
        }
        stage("Building"){
            steps {
                script {
                    sh """
                      echo " This is Building stage"
                      echo "$ENVI"
                    """
                }
            }
        }
        stage("Deployment"){
            steps {
                script {
                    sh """
                      echo " This is Deployment stage"
                      echo "$ENVI"
                      
                    """
                }
            }
        }
    }
}