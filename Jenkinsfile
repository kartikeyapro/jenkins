pipeline {
    agent any

    tools {
        maven 'maven-3.8.4'
    }

    stages {
        stage('Git Clone') {
		    steps {
			git 'https://github.com/ksproapp/ks.git'
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
					
		stage('Maven Validate') {
		    steps {
				sh 'mvn validate'
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
					
		stage('Maven Package') {
		    steps {
				sh 'mvn package'
                    }
					}
					
		stage('Maven Deploy') {
		    steps {
				sh 'mvn deploy'
                    }
					}
					

     }
}