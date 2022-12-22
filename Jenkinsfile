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
				        sh "sudo yum install httpd -y"
					sh "sudo cp index.html /var/www/html/index.html"
				        sh "sudo chmod -R 777 /var/www/html/index.html"
			}
		
		}
		
		stage ("start"){
		steps {
				sh "sudo service httpd start"
		
		}
		
		}

}

}
