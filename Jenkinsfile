pipeline {
    agent any
    
    options {
        timestamps()
        timeout(time: 5, unit: 'MINUTES')
        buildDiscarder(logRotator(daysToKeepStr: '7', artifactDaysToKeepStr: '7'))
    }
    
    parameters {
        string(name: 'pr_number', defaultValue: '0', description: '', trim: true)
    }

    stages {
        stage('stage 1') {
            steps {
                echo 'stage 1'
                echo "PR: ${params.pr_number}"
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('stage 2') {
            steps {
                echo 'stage 2'
                dir('actions-sandbox') {
                    git branch: 'main',
                        url: 'https://github.com/SnowCait/actions-sandbox/'
                    sh 'ls -la'
                }
            }
        }
    }
}
