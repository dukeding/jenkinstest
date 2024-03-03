pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                timeout(time: 10, unit: 'SECONDS') {
                    retry(5) {
                        sh './testRetry.sh'
                    }
                }
            }
        }
    }
}
