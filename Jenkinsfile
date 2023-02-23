pipeline {
	agent {
		label {
			label "slave1"
		}
	}
	stages {
		stage('CleanWorkspace') {
            steps {
                cleanWs()
		}
		}
		stage ("build maven project") {
			steps {
			    sh "export PATH=$PATH:/opt/apache-maven-3.9.0/bin"
			sh "sudo mvn clean package"
		}
		}
			}
}
