@Library('test-lib@master')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('stuff') {
            steps {
                 //maxTest 'max'
                echo 'test'
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
