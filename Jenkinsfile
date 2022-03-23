pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/ljdihingia/SpringPetClinic.git'
                }           
        }   
        stage('Build'){
            steps{
                sh 'mvn compile'
                }
        }
        stage ('Test'){
            steps{
                sh 'mvn test'
                }
        }
        stage ('Deploy'){
        
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }    
        }
        
        
    }
    
}
