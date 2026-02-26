pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
         
          
    }

    environment {
        COURSE = "jenkins"
    }
    stages {
    stage('Build') {
    steps {
        echo "Building"
        echo "${env.COURSE}"
    }
           }
        }
        stage('Test') { 
            steps {
                sh """
                 echo "Testing"
                    """
                 
            }
        }
        stage('Deploy') { 
            steps {
                sh """
                echo "Deploying"
                """
            }
        }
    

    post {
        always {
            echo 'I will Always say Hello Again'
            cleanWs()
        }
        success {
            echo 'I will Run if Success'
        }
        failure {
            echo 'I will Run if Failure'
        }
    }
}
