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
    parameters{
        string(name: 'USER', defaultValue: 'Lavanya', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage('build stage'){
            steps{
                script{
                    sh """
                        echo "building by ${param.USER}"
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