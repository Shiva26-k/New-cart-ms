pipeline{
    agent any 
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage('Deplyoing in DEV'){
            steps{
                echo "Successfully deployed in DEV"
            }
        }
        stage('DEploying in Production'){
            when{
                anyOf{
                    branch 'production'
                    environment name :'DEPLOY_TO' , value : 'release'
                }
            }
            steps{
                echo "Successfully deployed in PRODUCTION"
            }
        }
    }
}
