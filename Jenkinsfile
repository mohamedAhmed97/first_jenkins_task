pipeline{
    agent any
    environment{
         DB_ENGINE    = 'sqlite'
    }
    stages{
        stage("buliding"){
            steps{
                echo "========executing Buliding ${DB_ENGINE}========"
            }
        }
         stage("testing"){
            steps{
                echo "========executing Testing ... ${GIT_BRANCH}========"
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
