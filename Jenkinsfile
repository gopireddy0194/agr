pipeline
{
    agent any
    
    stages{
        stage('Continous download1')
        {
            steps
            {
		echo " This job will pick files from other repo"
                git 'https://github.com/gopireddy0194/agr.git'
            }
        }
	stage('Validate-again')
	{
		steps
		{
		   sh label: '', script: 'mvn validate'
		}
	}
        stage('compile-1')
        {
            steps
            {
              sh label: '', script: 'mvn compile'  
            }
            
        }
        stage('test')
        {
            steps
            {
                sh label: '', script: 'mvn test'
            }
        }
        stage('final')
        {
            steps
            {
		sh label: '', script: 'mvn package'

                echo " This is a file created in my own repo and used to fetch code from other repo"
            }
        }
    }
} 
