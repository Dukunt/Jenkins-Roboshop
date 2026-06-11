pipeline {
    agent any
    stages{
        stage("testing"){
            steps {
                script {
                    sh """
                      echo " This is Testing stage"
                      echo " Successful"
                    """
                }
            }
        }
        stage("Building"){
            steps {
                script {
                    sh """
                      echo " This is Building stage"
                      echo " Successful"
                    """
                }
            }
        }
        stage("Deployment"){
            steps {
                script {
                    sh """
                      echo " This is Deployment stage"
                      echo " Successful"
                    """
                }
            }
        }
    }
}