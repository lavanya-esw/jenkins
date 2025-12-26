pipeline{
    agent{
        node{
            label 'AGENT-1'
        }
    }
    environment{
        COURSE = "jenkins"
    }
    options{
        timeout(time: 20, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    stages{
        stage('build stage'){
            steps{
                script{
                    sh """
                        echo "building....."
                        echo ${COURSE}
                    """
                }
            }
        }
        stage('test stage'){
            steps{
                script{
                    sh """
                        echo "testing....."
                        echo ${COURSE}
                    """
                }
            }
        }
        stage('deploy stage'){
            steps{
                script{
                    sh """
                        echo "deploying....."
                        echo ${COURSE}
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
        aborted{
            echo "build is aborted...."
        }

    }
}