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
        stage('try') {
            steps {
                echo 'Hello world'
                script {
                    try {
                      sh('false')
                    } catch (ex) {
                      unstable('Script failed!')
                    }
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
            slackSend channel: "#max-bot", color: "red", message: ":x: Bad"
        }
        unstable {
            slackSend channel: "#max-bot", color: "warning", message: ":warning: You have failing tests"
        }
    }
}
