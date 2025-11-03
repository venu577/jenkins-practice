pipeline {
    agent  {
        label 'AGENT-1'
    }

     environment { 
        COURSE = 'jenkins'
    }

     options {
        timeout(time: 10, unit: 'SECONDS') 
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                       echo 'Building..'
                       env
                       sleep 10
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying....'
                }  
            }
        }
    }

     post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'Hello Success'
        }
        failure { 
            echo 'Hello Failure'
        }
    }
}