pipeline{
    agent any
    parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['Testing', 'Dev'], description: 'Pick something')

    }
    environment{
         DB_ENGINE    = 'sqlite'
    }
    stages{
        stage("buliding"){
            steps{
                echo "========executing Buliding ${DB_ENGINE}========"
                echo "${params.PERSON}"
            }
        }
         stage("testing"){
            when{
                expression{
                    params.CHOICE=="Testing"
                }
            }
            steps{
                echo "========executing Testing ... ${GIT_BRANCH}========"
            }
        }
         stage("development"){
            when{
                expression{
                    params.CHOICE=="Dev"
                }
            }
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
