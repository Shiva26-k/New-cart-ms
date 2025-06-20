pipeline{
    agent any
    stages{
        stage('Deploying_dev'){
            steps{
                echo "Deploying in dev environment"
            }
        }
        stage('Deploying_prod'){
            steps{
                when{
               expression {BRANCH_NAME ==~ /(production|staging)/}
                 echo "Deploying in prod environment"
                }
            }
        }
    }
}
