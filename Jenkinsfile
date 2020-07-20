pipeline {
    agent any

    env.MYTOOL_VERSION = '1.33'
    
    stages {

        stage('build') {
            steps {
                echo 'Fazendo o step 1 build...'
                sh 'echo ${MYTOOL_VERSION}'
                echo 'Fazendo o step 3 build...'
                echo 'Fazendo o step 4 build...'
                sh 'ls -l /tmp'
            }
        }

        // stage('deploy') {
        //     steps {
        //         echo 'Fazendo o deploy 1...'
        //         echo 'Fazendo o deploy 2...'
        //         echo 'Fazendo o deploy 3...'
        //     }
        // }

    }
}