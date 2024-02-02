pipeline {
  agent {
    node {
        label 'AGENT-1'        
    }
}
environment { 
        GREETING='HELLo JENKINS'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "$GREETING"
                    echo "I wrote Shell"
                    env    

                """
            }
        }
    }


//POST _ AFTER BUILD
    post { 
        always { 
                 echo 'I will always say Hello again!'
                }
        failure { 
                echo 'Failure Status'
                }
        success { 
                echo 'Success Status'
                }
    }
}