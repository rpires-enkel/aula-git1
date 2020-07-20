env.MYTOOL_VERSION = '1.33'

pipeline {
    agent any
    environment {
        CC = """${sh(
                returnStdout: true,
                script: 'echo "clang"'
            )}"""
    }

    stages {
        stage('build') {
            steps {
                echo 'Fazendo o step 1 build...'
                sh 'echo ${MYTOOL_VERSION}'
                sh 'ls -l /tmp'
                sh 'printenv'
            }
        }

        stage('deploy') {
            when {
                    expression {
                        currentBuild.result == null || currentBuild.result == 'SUCCESS'
                    }
                }

            steps {
                echo currentBuild.result
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                sh 'echo "uaua"'
            }
        }
    }

}