#!groovy

pipeline {
    agent any
    stages {
        stage('load groovy') {
            steps {
                echo '===== load groovy ====='
                script {
                    util = load 'groovy/home/rud/PipelineUtil.groovy'
                    String result = util.doSomething()
                    echo "result:$result"
                }
            }
        }
    }
}
