pipeline {
    agent any

    stages {
        stage('Build-environment') {
            steps {
                echo "Building the application"
            }
        }

        stage('Code_Analysis') {
            steps {
                echo "Analysing the code"
            }
        }

        stage('Building_DockerFile') {
            steps {
                echo "Building Docker image"
            }
        }

        stage('Deploying_Dev') {
            steps {
                echo "Deploying to DEV environment"
            }
        }

        stage('Deploying_Test') {
            steps {
                echo "Deploying to TEST environment"
            }
        }

        stage('Deploying_Stage') {
            when {
                branch pattern: 'release-.*', comparator: 'REGEXP'
            }
            steps {
                echo "Deploying to STAGE environment"
            }
        }

        stage('Deploying_Prod') {
            when {
                tag pattern: '^v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}$', comparator: 'REGEXP'
            }
            steps {
                echo "Deploying to PRODUCTION: ${env.GIT_TAG_NAME}"
            }
        }
    }
}
