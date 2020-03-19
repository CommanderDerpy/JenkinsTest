@Library('test-lib@master')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('stuff') {
            steps {
                 echo 'hiii!'
            }
            steps {
                 maxTest 'max'
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
