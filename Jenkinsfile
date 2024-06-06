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
        stage('deploy') {
            steps {
                echo 'Hello Deploy'
                execute_stage('deploy',params.skip_test)
            }
        }
    }
}
def execute_stage(stage_name,skip){
    stage(stage_name){
        if(skip){
            echo "skipping ${stage_naem} stage"
            return
        }
    }
}
