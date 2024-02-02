pipeline {
  agent {
    node {
        label 'AGENT-1'        
    }
}
environment { 
        GREETING='HELLo JENKINS'
    }
options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
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
                    sleep 10   

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