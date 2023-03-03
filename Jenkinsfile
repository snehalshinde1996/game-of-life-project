
    pipeline {
	agent {
	  label {
        label ("built-in") 
        customWorkspace '/mnt/project' 
        
	}
  }
       stages {
        stage ("cleaning workspace") 
        {
         steps {
           cleanWs()
         }
        }
          stage ("checkout from scm")
       {
          steps {
           checkout scm
        }
      }
         stage ("build war file") {
         steps {
         sh 'sudo mvn clean'
         sh 'sudo mvn package'
       }
       }
         stage ("copy war file to slave") {
         steps {
		 
          sh 'sudo scp -i /opt/jenkins.pem /mnt/project/gameoflife.war ec2-user@172.31.46.224:/opt/gameoflife'
    
      }
       }


     

        
    }
}
