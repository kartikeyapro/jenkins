pipeline {
    agent any
	#tools{
	#maven 'maven-3.8.1'
	#}
    stages {
        stage('gitclone') {
            steps {
                git branch: 'main', credentialsId: 'gitpass', url: 'https://github.com/ksproapp/myapp.git'
            }
        }
		 stage('Maven Version') {
            steps {
                sh 'mvn --version'
            }
			}
         stage('Maven Clean') {
            steps {
                sh 'mvn clean'
            }
			}
         stage('Maven Compile') {
            steps {
                sh 'mvn compile'
            }
			}
         stage('Maven Test') {
            steps {
                sh 'mvn test'
            }
			}
         stage('mvn package') {
            steps {
                sh 'mvn package'
            }
			}
		}
    }