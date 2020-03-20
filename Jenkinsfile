@Library('test-lib')_

pipeline {
    agent { docker { image 'node:6.3' } }
    parameters {
        string(name: 'VERSION', defaultValue: '', description: 'Version to use if Override is chosen. - Default: ""')
    }
    stages {
        stage('Demo') {
            steps {
                echo 'Hello world'
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
