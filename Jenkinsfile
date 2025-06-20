pipeline{
    agent any
    stages{
        stage('Deploying_dev'){
            steps{
                echo "Deploying in dev environment"
            }
        }
        stage('Deploying_prod'){
            when{
               expression {BRANCH_NAME ==~ /(production|staging)/} 
                }
            steps{
                echo "Deploying in prod environment"
            }
        }
    }
}
