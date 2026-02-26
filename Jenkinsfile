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
                    echo "Building"
                echo "Jenkins environment variable COURSE: ${env.COURSE}"
                }
                
            }
        }

        stage('Test') { 
            steps {
                 script {
                    echo "Testing"
                echo "Jenkins environment variable COURSE: ${env.COURSE}"
                }
            }
        }

        stage('Deploy') { 
            steps {
                 script {
                    echo "Deploying"
                echo "Jenkins environment variable COURSE: ${env.COURSE}"
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