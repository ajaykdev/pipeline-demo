pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
				steps {
					bat 'mvn deploy -DmuleDeploy -Denv=Dev -DconnectedApp.clientId=efef7b08ade74b0b8ebe3745334bea18 -DconnectedApp.clientSecret=3e8C23625CEA407cAa6b529a08312Aa9 -DconnectedApp.grantType=client_credentials'
				}
					}
    }
}