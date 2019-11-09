pipeline {
    agent any
	stages {
    stage ('Compile Stage') {maven

       steps {
         withmaven(maven : 'maven') {
           sh 'mvn clean compile'
       }
     }
   } 

	stage ('Testing Stage') {

         steps {
           withmaven(maven : 'maven') {
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
 
