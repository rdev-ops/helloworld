pipeline {
    agent any
	stages {
    stage ('Compile Stage') {

       steps {
         with maven(maven : 'maven') {
           sh 'mvn clean compile'
       }
     }
   } 

	stage ('Testing Stage') {

         steps {
           with maven(maven : 'maven') {
		sh 'mvn test'
           
	 }	
       }
     }

	stage ('Deployment Stage') {
          steps {
             with maven(Maven : 'maven') {
		  sh 'mvn deploy'
     }
    }
   }
  }
 }	    
 
