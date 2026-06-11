pipeline {
    agent any
    stages{
        stage("testing"){
            steps {
                script {
                    sh """
                      echo " This is Testing stage"
                    """
                }
            }
        }
        stage("Building"){
            steps {
                script {
                    sh """
                      echo " This is Building stage"
                    """
                }
            }
        }
        stage("Deployment"){
            steps {
                script {
                    sh """
                      echo " This is Deployment stage"
                    """
                }
            }
        }
    }
}