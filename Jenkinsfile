pipeline {
    agent any
	stages {
    stage ('Compile Stage') {Maven

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
             with maven(maven : 'maven') {
		  sh 'mvn deploy'
     }
    }
   }
  }
 }	    
 
