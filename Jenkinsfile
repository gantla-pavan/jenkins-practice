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
                script {
                    sh """
                 echo "Testing"
                    """

                }
                
                 
            }
        }
        stage('Deploy') { 
            steps {
                script {
                     sh """
                    echo "Deploying"
                        """
                }
               
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
