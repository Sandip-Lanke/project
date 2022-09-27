pipeline {
    agent {
	    label 'built-in'
		}
	stages {
	  stage ('install-appache'){
	  steps {
	     sh "yum install httpd -y"
		  sh "yum install tree -y"
	  }
	  
	  }
	  stage ('start-appache'){
	  steps {
	     sh "service httpd start"
	  }
	  
	  }
	  stage ('deploy-index.html'){
	  steps {
	     sh "cp -r index.html /var/www/html/"
		 sh "chmod -R 777 /var/www/html/index.html"
		  
	  }
	  
	  }
	
	}
	
}

