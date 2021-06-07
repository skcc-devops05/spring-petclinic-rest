pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './mvnw clean compile'
            }
        }
        stage('Unit Test') {
		    steps {
		        sh './mvnw test'
		    }
		    post {
		        always {
		            junit 'target/surefire-reports/*.xml'
		        }
            }
        }
	}
}