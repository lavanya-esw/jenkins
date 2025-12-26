pipeline{
    agent{
        node{
            label 'AGENT-1'
        }
    }
    stages{
        stage('build stage'){
            steps{
                script{
                    sh """
                        echo "building....."
                    """
                }
            }
        }
        stage('test stage'){
            steps{
                script{
                    sh """
                        echo "testing....."
                    """
                }
            }
        }
        stage('deploy stage'){
            steps{
                script{
                    sh """
                        echo "deploying....."
                    """
                }
            }
        }
    }
    post{
        always{
            echo "I will always run!!!"
            // cleanws()
        }
        success{
            echo "build is success....."
        }
        failure{
            echo "build is failed......"
        }

    }
}