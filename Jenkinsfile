pipeline {
    agent any
    environment {
        appversion = ""
        ACC_ID = 079662785129
        region = "us-east-1"
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
                        withAWS(credentials:'aws-creds ', region: "${region}") {
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