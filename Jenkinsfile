pipeline{
    agent any 
    environment{
        DEPLOY_TO = 'release'
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
                    branch 'release'
                    environment name :'DEPLOY_TO' , value : 'production'
                }
            }
            steps{
                echo "Successfully deployed in PRODUCTION"
            }
        }
    }
}
