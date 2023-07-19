pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    git 'https://github.com/PotdarDatta/GitDemo.git'
     
                  bat "./mvn clean install"	
                echo 'Buiding the project with maven compile'
            }
        }
        stage('Test') {
            steps {

		bat "./mvn test"	
                echo 'testing the project with maven'
            }
        }
        stage('Containerize') {
            steps {
		bat "docker build -t petadoption-master-image"
                echo 'deploy the app with Docker'
            }
        }
	 stage('Deploy') {
            steps {
		 bat "docker run -d -p 9090:9090 petadoption-master-image"

		echo 'Deploy the app with docker'
            }
        }	

    }
}
