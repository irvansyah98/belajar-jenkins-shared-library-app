pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Build") {
            steps {
                echo "Hello Build"
            }
        }
        stage("Test") {
            steps {
                echo "Hello Test"
            }
        }
        stage("Deploy") {
            steps {
                echo "Hello Deploy"
            }
        }
    }
    post {
        always {
            echo "i will always say hello"
        }
        success {
            echo "yay, success"
        }
        failure {
            echo "oh no, failure"
        }
        cleanup {
            echo "don't care success or error"
        }
    }
}