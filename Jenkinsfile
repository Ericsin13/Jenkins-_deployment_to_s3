pipeline {
agent any {

   tools{
      maven 'maven-3.9.4'
   } 
   stages {
      stage (build) {
         steps {
	    sh 'mvn clean package'
	 }
      }
      stage (testing) {
         steps {
	    sh 'mvn test'
	 }
      }
      stage (deploy) {
         steps {
	    sh "aws s3 cp free.html s3://s3jenkinsdemo"
	    }
       	}
     }
  }
