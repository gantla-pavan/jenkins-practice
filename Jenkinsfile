pipeline {
    agent {
        label 'AGENT-1'
    }

    environment {
        COURSE = "jenkins"
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                    echo "Building"
                    echo  $COURSE
                    env
                    
                    """
                }  
                
            }
        }

        stage('Test') { 
            steps {
                 script {
                    sh """
                    echo "Building"
                    echo  $COURSE
                    
                    """
                    
                   
                }
            }
        }

        stage('Deploy') { 
            steps {
                 script {
                    sh """
                    echo "Building"
                    echo  $COURSE
                    
                    """
                    
                }
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