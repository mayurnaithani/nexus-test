pipeline{

      agent any
        
        stages{

              stage('Build and push to nexus'){
                  steps {
			  script {
				  withMaven(maven: 'maven3') {
              			                   sh "mvn clean install"
					 }
			  }
              	        }  
              }	
	   
			    
			
            }	       	     	         
}
