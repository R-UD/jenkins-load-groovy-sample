#!groovy

def modules = [:]

pipeline {
    agent any
    stages {
        stage('load groovy') {
            steps {
                echo '===== load groovy ====='
                script {
                    modules.util = load 'groovy/home/rud/PipelineUtil.groovy'
                    String result = util.doSomething()
                    echo "result:$result"
                }
            }
        }
        stage('do in other stage') {
            steps {
                echo '===== do in other stage ====='
                script {
                    String result = util.doSomething()
                    echo "result2:$result"
                }
            }
        }
    }
}
