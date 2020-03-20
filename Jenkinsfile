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
                    log.info params.VERSION
                    log.warning params.VERSION
                }
            }
        }
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
    post {
        success {
            script {
                slackSend channel: "#max-bot", color: "good", message: ":white_check_mark: Good!"
            }
        }
        failure {
            slackSend channel: "#max-bot", color: "bad", message: ":x: Bad"
        }
    }
}
