pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				sh '''g++ -c pipeline_PES1UG20CS433.cpp
				g++ pipeline_PES1UG20CS433.o'''
				build 'PES1UG20CS433-1'
				echo 'Build stage successful'
			}
                }
		stage('Test') {
			steps {
				sh './test'
				echo 'Test stage successful'
			}
                }
		stage('Deploy') {
			steps {
				echo 'Deploy stage successful'
			}
                }
        }
	post {
		failure {
			echo 'Pipeline failed'
		}
	}
}
