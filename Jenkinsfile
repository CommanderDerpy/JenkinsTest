@Library('test-lib@master')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('Demo') {
            steps {
                echo 'Hello world'
                script {
              script { 
                    log.info 'Starting'
                    log.warning 'Nothing to do!'
                }
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
