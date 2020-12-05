#!/usr/bin/env groovy

JIRA_TICKET = 'Not Applicable'

pipeline {
    agent any
    options {
        timeout(time: 60, unit: 'MINUTES')
        retry(0)
        quietPeriod(0)
        buildDiscarder(logRotator(numToKeepStr: '30', daysToKeepStr: '90'))
        timestamps()
    }

    stages {
        stage("Create Jira ticket for cleanup") {
            steps {
                script {
                    echo "${JIRA_TICKET}"
                }
            }
        }
    }
}
