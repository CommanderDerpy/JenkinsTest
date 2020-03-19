@Library('JenkinsLibrary') _

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('stuff') {
              filename.checkout
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
