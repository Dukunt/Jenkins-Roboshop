pipeline {
    agent any
    stages{
        stage("testing"){
            steps {
                script {
                    sh """
                      echo " This is Testing stage"
                      echo " Successfully done"
                    """
                }
            }
        }
        stage("Building"){
            steps {
                script {
                    sh """
                      echo " This is Building stage"
                      echo " Successfully done"
                    """
                }
            }
        }
        stage("Deployment"){
            steps {
                script {
                    sh """
                      echo " This is Deployment stage"
                      echo " Successfully done"
                      
                    """
                }
            }
        }
    }
}