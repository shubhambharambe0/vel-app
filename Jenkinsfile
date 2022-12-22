pipeline {
agent{
label{
		label "slave-1"
		customWorkspace "/mnt/jenkin-slave1"
}
}

stages {

		stage ("deploy-1"){
			steps {
				        sh "yum install httpd -y"
					sh "cp -r index.html /var/www/html/"
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
