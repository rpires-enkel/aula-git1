env.MYTOOL_VERSION = '1.33'

pipeline {
    agent any

    stages {

        stage('build') {
            steps {
                echo 'Fazendo o step 1 build...'
                sh 'echo ${MYTOOL_VERSION}'
                echo 'Fazendo o step 3 build...'
                sh 'ls -l /tmp'
            }
        }

        stage('deploy') {
            when {
                    expression {
                        currentBuild.result == null || currentBuild.result == 'SUCCESS'
                    }
                }

            steps {
                sh 'echo "uaua"'
            }
        }

    }
}