pipeline {
    agent any
        parameters {
            booleanParam defaultValue: true, name: 'skip_test'
        }

    stages {
        stage('build') {
            steps {
                echo 'Hello Build'
            }
        }
        stage('test') {
            when {expression {params.skip_test !=true}}
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
