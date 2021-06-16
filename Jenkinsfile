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
                    modules.cpsSample = load 'groovy/home/rud/CpsClassSample.groovy'
                    String result = modules.util.doSomething()
                    String result2 = modules.cpsSample.getHello()
                    echo "result:$result"
                    echo "result2:$result2"
                }
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
