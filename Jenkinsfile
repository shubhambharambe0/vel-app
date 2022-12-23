pipeline {
agent{
label{
		label "slave-1"
		customWorkspace "/mnt/myproject"
}
}

stages {

		stage ("deploy-1"){
			steps {
				        sh "sudo yum install httpd -y"		
			}
		
		}
		
		stage ("start"){
		        steps {
			        sh "sudo cp -r /mnt/myproject/index.html /var/www/html/index.html"
				sh "sudo chmod -R 777 /var/www/html/index.html"
				sh "sudo service httpd start"
		
		}
		
		}

}

}
