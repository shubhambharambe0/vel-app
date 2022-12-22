pipeline {
agent{
node{
				label "slave-1"
				customWorkspace "/mnt/jenkin-slave1"
}
}

stages {

		stage ("deploy-1"){
			steps {        
				        sh "git remote add origin https://github.com/shubhambharambe0/vel-app.git"
				        sh "git clone https://github.com/shubhambharambe0/vel-app.git"
				        sh "yum install httpd -y"
					sh "cp index.html /var/www/html/"
				        sh "chmod -R 777 /var/www/html/index.html"
			}
		
		}
		
		stage ("start"){
		steps {
				sh "service httpd start"
		
		}
		
		}

}

}
