pipeline{

agent any
 stages{
    stage('continous download')
    {

	echo " This job will pick files from other repo"
        sh label: '', script: 'ls -a'
              
       sh label: '', script: 'mvn compile'  
    }
 }

}
