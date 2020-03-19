@Library('test-lib')_

pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('stuff') {
              maxTest 'max'
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}
