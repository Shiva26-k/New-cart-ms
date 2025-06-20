pipeline{
    agent any
    stages{
        stage('Build-environmet'){
            steps{
                echo "Building the application"
            }
        }
        stage('Code_Analysis'){
            steps{
                echo "Analysing the Code"
            }
        }
        stage('Building_DockerFile'){
            steps{
                echo "Docker Building"
            }
        }
        stage('Deploying_Dev'){
            steps{
                echo "Deploying DEV environment"
            }
        }
        stage('Deploying_Test'){
            steps{
                echo "Deploying TEST environment"
            }
        }
        stage('Deplyoing_stage'){
            when{
                branch 'release-*'
            }
            steps{
                echo "Deploying STAGE environment"
            }
        }
        stage('Deploying_Prod'){
            when{
                //tag pattern
                //vx.x.x
                //v1.2.3 is correct
                //v.1.2.3 is wrong
                tag pattern : "v\\d{1,2}.\\d{1,2}.\\d{1,2}" , comparator: "REGEXP"
            }
            steps{
                echo "Deploying PRODUCTION  ${env.GIT_TAG_NAME} environmnt"
            }
        }
    }
}
