pipeline {
    agent any
	tools {
		maven 'mvn_home'
		}

    stages {
        stage('SCM-Checkout') {
            steps {
                git branch: 'main', credentialsId: 'git-credentials', 
				url: 'https://github.com/vikas99341/my-app-dj.git'
            }
        }
        stage('maven-steps') {
            steps {
                sh 'mvn compile test package'
            }
        }
    }
}
