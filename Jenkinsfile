pipeline{
    agent any
    environment{
        name = "Shiva"
        courses = "devops and gcp"
    }
    stages{
        stage('Build'){
             environment{
            cloud ="gcp"
        } 
            steps{
                echo "Welconme ${name}"
                echo "you registered for ${courses}"
                echo "You certificated in ${cloud}"
            }
        }
        stage('sonar'){
            steps{
                echo "Welconme ${name}"
                echo "you registered for ${courses}"
                echo "Your Branch name ${env.BRANCH_NAME}"
            }
        }
    }
}
