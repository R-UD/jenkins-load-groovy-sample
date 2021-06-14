#!groovy

PipelineUtil util = load 'groovy/home/rud/PipelineUtil.groovy'

pipeline {
    agent any
    stages {
        stage('load groovy') {
            steps {
                echo '===== load groovy ====='
                script {
                    String result = util.doSomething()
                    echo "result:$result"
                }
            }
        }
    }
}
