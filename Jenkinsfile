#!groovy
@Library('shared-lib-sample@master') _

def modules = [:]

pipeline {
    agent any
    stages {
        stage('load groovy') {
            steps {
                echo '===== load groovy ====='
                script {
                    modules.util = load 'groovy/home/rud/PipelineUtil.groovy'
                    String result = modules.util.doSomething()
                    echo "result:$result"

                }

                sayHello 'hello world'
            }
        }
        stage('do in other stage') {
            steps {
                echo '===== do in other stage ====='
                script {
                    String result = modules.util.doSomething()
                    echo "s2:result:$result"
                }
            }
        }
    }
}
