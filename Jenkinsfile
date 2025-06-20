pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage('deploying'){
            when{
                not{
                equals expected:"prod" , actual:"${DEPLOT_TO}"
                }
            }
            steps{
                echo "Deploying in production"
            }
        }
    }
}
