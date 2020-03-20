@Library('test-lib@master')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('Demo') {
            step {
                echo 'Hello world'
                sayHello 'Dave'
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
