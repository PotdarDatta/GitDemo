pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    
     
                 	
                echo 'Buiding the project with maven compile'
            }
        }
        stage('Test') {
            steps {

			
                echo 'testing the project with maven'
            }
        }
        stage('Containerize') {
            steps {
		
                echo 'deploy the app with Docker'
            }
        }
	 stage('Deploy') {
            steps {
		

		echo 'Deploy the app with docker'
            }
        }	

    }
}
