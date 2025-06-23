pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Building the application"
            }
        }
        stage('PARALLELSCANS'){
            parallel{
                 stage('codeAnalysis'){
                    steps{
                        echo "Running the code analysis"
                        sleep 10
                     }
                }
                stage('SecurityScan'){
                    steps{
                        echo "Running Securityscan"
                        sleep 10
                    }
                }
                stage('PerformanceTest'){
                    steps{
                        echo "running performance test"
                        sleep 10
                    }
                }
            }
        } 
    }
}
