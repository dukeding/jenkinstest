pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh './testRetry.sh'
                }

                timeout(time: 1, unit: 'MINUTES') {
                    sh './testTimeout.sh'
                }
            }
        }
    }
}
