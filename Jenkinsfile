pipeline{
    agent any
    stages{
        stage("buliding"){
            steps{
                echo "========executing Buliding========"
            }
        }
         stage("testing"){
            steps{
                echo "========executing Testing========"
            }
        }
         stage("development"){
            steps{
                echo "========executing Development========"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
