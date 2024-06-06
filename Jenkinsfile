pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello Build'
            }
        }
        stage('test') {
            parallel {
                stage('unit test') {
                    steps {
                        echo 'Hello Unit test'
                    }
                }
                stage('integration test') {
                    steps {
                        echo 'Hello Integration test'
                    }
                }
            }
        }
        stage('deploy') {
            steps {
                echo 'Hello Deploy'
            }
        }
    }
}
