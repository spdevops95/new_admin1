pipeline {
    agent none

    stages {
        stage('Build') {
            agent {
                kubernetes {
                    label 'my-kubernetes-agent'
                }
            }
            steps {
                echo 'Executing the build command...'
                sh 'your_build_command'
                // Replace 'your_build_command' with the actual build command
            }
        }

        stage('Test') {
            agent {
                kubernetes {
                    label 'my-kubernetes-agent'
                }
            }
            steps {
                echo 'Executing the test command...'
                sh 'your_test_command'
                // Replace 'your_test_command' with the actual test command
            }
        }

        stage('Deploy') {
            agent {
                kubernetes {
                    label 'my-kubernetes-agent'
                }
            }
            steps {
                echo 'Executing the deployment command...'
                sh 'your_deploy_command'
                // Replace 'your_deploy_command' with the actual deployment command
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Ready for the next steps.'
            // Add success post-build actions here
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
            // Add failure handling or notifications here
        }
    }
}

