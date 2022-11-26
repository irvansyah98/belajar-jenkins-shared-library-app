pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Hello") {
            steps {
                echo "Hello World"
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