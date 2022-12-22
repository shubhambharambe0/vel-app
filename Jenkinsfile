pipeline {
agent{
node{
				label "slave-1"
				customWorkspace "/mnt/jenkin-slave1/hubserver"
}
}

stages {

		stage ("deploy-1"){
			steps {
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
