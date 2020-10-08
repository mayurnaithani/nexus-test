pipeline{

      agent any
        
        stages{

              stage('Build and push to nexus'){
                  steps{
                         withMaven(maven: 'maven3') {
						 sh "mvn clean install"
					 }    
                 	
               	 }  
              }	
		
            }	       	     	         
}