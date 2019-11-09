pipeline {
    agent any
	stages {
    stage ('Compile Stage') {

       steps {
         with Maven(maven : 'maven') {
           sh 'mvn clean compile'
       }
     }
   } 

	stage ('Testing Stage') {

         steps {
           with Maven(maven : 'maven') {
		sh 'mvn test'
           
	 }	
       }
     }

	stage ('Deployment Stage') {
          steps {
             with Maven(Maven : 'maven') {
		  sh 'mvn deploy'
     }
    }
   }
  }
 }	    
 
