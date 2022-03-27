pipeline
	{
	agent{label 'master'}
	tools{maven 'm3'}
	stages{
		stage('Checkout'){
			steps{
				git branch:'main' , url: 'https://github.com/ljdihingia/SpringPetClinic.git'
			}
		}

		stage('Build'){
			steps{
				sh 'mvn compile'
			}
		}

		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}

		stage('Package'){
			steps{
				sh 'mvn package'
			}
		}

		stage('Deploy'){
			steps{			
				echo 'Deployed'
			}
		}
	}
	
}