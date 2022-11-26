pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Build") {
            steps {

                script {
                    for (int i = 0; i < 10; i++) {
                        echo("Script ${i}")
                    }
                }

                echo "Start Build"
                sh("./mvnw clean compile test-compile")
                echo "Finish Build"
            }
        }
        stage("Test") {
            steps {
                echo "Start Test"
                sh("./mvnw test")
                echo "Finish Test"
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploy"
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