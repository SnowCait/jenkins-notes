pipeline {
    agent any
    
    options {
        timestamps()
        timeout(time: 5, unit: 'MINUTES')
        buildDiscarder(logRotator(daysToKeepStr: '7', artifactDaysToKeepStr: '7'))
    }
    
    parameters {
        string(name: 'PR_NUMBER', defaultValue: '0', description: '', trim: true)
    }

    stages {
        stage('stage 1') {
            steps {
                echo 'stage 1'
                echo "PR: ${PR_NUMBER}"
            }
        }
        stage('stage 2') {
            steps {
                echo 'stage 2'
            }
        }
    }
}
