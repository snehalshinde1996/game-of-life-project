pipeline {
	agent {
		label {
			label "slave1"
		}
	}
	stages {
		stage ("build maven project") {
			steps {
			    sh "rm -rf /opt/jenkins-slave/workspace/assignment1(22.02.23)/*"
			    /*sh "export PATH=$PATH:/opt/apache-maven-3.9.0/bin"*/
			    sh "sudo git clone https://github.com/ketank185/game-of-life_maven_project.git" 
			    sh "sudo mvn clean package"
		}
		}
			}
}
