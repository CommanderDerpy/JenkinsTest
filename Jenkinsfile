@Library('test-lib@master')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('Demo') {
            steps {
                echo 'Hello world'
                script {
                    maxTest.call 'Dave'
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
