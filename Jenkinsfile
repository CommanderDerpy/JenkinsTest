pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
