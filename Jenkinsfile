pipeline {
    agent any
    tools {
        maven 'maven-3.9.6'
    }
    stages {
        stage ( "Checkout the Project") {
            steps {
                git branch: 'main', url: 'https://github.com/asecurityguru/devsecops-jenkins-k8s-tf-sast-sonarcloud-repo'
            }
        }
		stage ( "Compile and Run Sonar Analysis" ) {
		steps {
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecopsshikhar -Dsonar.organization=devsecopsshikhar -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=0846fc4fb99e714cef3ead084f4c46424e1eb8a0'
		}
		}
    }
}
