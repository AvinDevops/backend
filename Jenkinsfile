pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disbaleConcurrentBuilds()
        ansiColor('xterm')
    }
    stages {
        stage('test') {
            steps {
                sh """
                 echo "this is testing"
                 ls -ltr
                """
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success {
            echo 'I will run when pipeline is success'
        }
        failure {
            echo 'I will run when pipeline is failure'
        }
    }
}