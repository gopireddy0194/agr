pipeline
{
    agent any
    
    stages{
	   
      	stage('Validate-again1')
	{
		steps
		{
		   sh label: '', script: 'mvn validate'
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
