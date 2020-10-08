pipeline{

      agent any
        
        stages{

              stage('Build and push to nexus'){
                  steps {
			  withMaven(maven: 'maven3') {
              			                   sh "mvn clean install"
					 }
			  nexusPublisher nexusInstanceId: 'mynexus', nexusRepositoryId: 'example-repo', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: 'target/project_sonar.war']], mavenCoordinate: [artifactId: 'project_sonar', groupId: 'sonar.test.demo', packaging: 'war', version: '1.0-SNAPSHOT']]]
			  
              	        }  
              }	
	   
			    
			
            }	       	     	         
}
