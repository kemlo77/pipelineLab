pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Invoke other pipeline') {
            steps {
                // build 'gatlingParameterized', parameters: [string(name: 'targeturl', value:'kalle anka')]
                build job: 'gatlingParameterized', parameters: [[$class: 'StringParameterValue', name: 'targeturl', value: 'hi hi hi' ]]
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}