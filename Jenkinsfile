pipeline {
  agent {
    node {
        label 'AGENT-1'        
    }
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
                echo 'Deploying....'
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