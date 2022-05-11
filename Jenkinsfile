pipeline {
    agent any
    
    options {
		timestamps()
		timeout(time: 5, unit: 'MINUTES')
		buildDiscarder(logRotator(daysToKeepStr: '7', artifactDaysToKeepStr: '7'))
    }

    stages {
        stage('stage 1') {
            steps {
                echo 'stage 1'
            }
        }
        stage('stage 2') {
            steps {
                echo 'stage 2'
            }
        }
    }
}
