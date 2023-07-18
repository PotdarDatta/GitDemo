pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    git 'https://github.com/PotdarDatta/GitDemo.git'
     
                  sh "./mvnw compile"	
                echo 'Buiding the project with maven compile'
            }
        }
        stage('Test') {
            steps {

		sh "./mvnw test"	
                echo 'testing the project with maven'
            }
        }
        stage('Containerize') {
            steps {
		sh "docker build -t petadoption-master-image"
                echo 'deploy the app with Docker'
            }
        }
	 stage('Deploy') {
            steps {
		 sh "docker run -d -p 9090:9090 petadoption-master-image"

		echo 'Deploy the app with docker'
            }
        }	

    }
}
