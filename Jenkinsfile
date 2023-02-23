pipeline {
	agent {
		label {
			label "slave1"
			customWorkspace "/opt/assignment1"
		}
	}
	stages {
		stage ("clean workspace"){
			steps {
			cleanWs()
			}
		}
		stage ("build maven project") {
			steps {
			    sh "export PATH=$PATH:/opt/apache-maven-3.9.0/bin"
			sh "git clone https://github.com/ketank185/game-of-life_maven_project.git"
			sh "mvn package"
		}
		}
			}
}
