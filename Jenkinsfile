
    pipeline {
	agent {
	  label {
        label ("built-in") 
        cutomWorkspace '/mnt/project' 
        
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
         sh 'mvn clean'
         sh 'mvn package'
       }
       }
         stage ("copy war file to slave") {
         steps {
          sh 'scp-i "jenkins.pem" /mnt/project/gameoflife.war ec2-user@13.127.51.148:/opt/gameoflife'
    
      }
       }


     

        
    }
}
