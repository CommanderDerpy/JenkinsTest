pipeline {
    agent { docker { image 'node:6.3' } }
    stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
