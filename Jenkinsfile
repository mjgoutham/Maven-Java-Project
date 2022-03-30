pipeline {
    agent any 
    stages {
        stage('checkout') {
 
            steps {
   sh 'git clone https://github.com/mjgoutham/hello-world-war.git'
            }
        }
		        stage('build') {
				
            steps {
  sh 'mvn clean package'
            }
        }
          

	    stage('DeployAppIntoTomcat'){
  steps{
  
   sh "/home/ubuntu/hello-world-war/target/hello-world-war-1.0.0.war /opt/tomcat/apache-tomcat-10.0.17/webapps"     
  }
  }
    }
}
