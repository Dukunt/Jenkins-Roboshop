pipeline {
    agent any
    environment {
        appversion = ""
        // # ACC_ID = 079662785129
    }

    stages {
        stage("Read version") {
            steps{
                script{
                    def jsonfile = readJSON file: 'package.json'
                    appversion= jsonfile.version
                    echo " App version is ${appversion}"

                }
            }
        }
        stage("Install dependencies") {
            steps{
                script {
                    sh"""
                     npm install
                    """
                }
            }

        }

        stage("Build the image") {
            steps{
                script{
                    sh"""
                     docker build -t catalogue:${appversion} .
                    """
                  /*  withAWS(credentials:' ',region: 'us-east-1') {
                        sh"""
                            aws ecr get-login-password --region ${region} | 
                            docker login --username AWS --password-stdin ${ACC_ID}.dkr.ecr.us-east-1.amazonaws.com
                            docker build -t ${ACC_ID}.dkr.ecr.${region}.amazonaws.com/roboshop/catalogue:${appversion} .
                            docker push ${ACC_ID}.dkr.ecr.${region}.amazonaws.com/roboshop/catalogue:${appversion}
                        """  */
                    }
                }
        }

        

    }
}