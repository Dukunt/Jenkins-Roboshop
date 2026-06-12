pipeline {
    agent any
    environment {
        ENVI = "dev"
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage("testing"){
            steps {
                script {
                    sh """
                      echo " This is Testing stage"
                      echo "$ENVI"
                      echo "${params.PERSON}"
                      echo "${params.BIOGRAPHY}"
                      echo "${params.PASSWORD}"
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
                      echo "${params.PERSON}"
                      echo "${params.BIOGRAPHY}"
                      echo "${params.PASSWORD}"
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