pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage('DeployToDev'){
            steps{
                echo "Deploying in Dev environment"
            }
        }
        stage('DeploytoProd'){
             when{
                allOf{
                    branch 'production'
                    environment name :'DEPLOY_TO' , value :'production'
                }
            }
            steps{
                echo "Deploying in prod environmennt"
            }
        }
    }
}
