pipeline {
agent{
label{
		label "built-in"
		customWorkspace "/mnt/myproject"
}
}

stages {

		stage ("deploy-1"){
			agent {
		
				label "slave-1"
				customWorkspace "/mnt/jenkin-slave1"
		
		
		}
			steps {
				        sh "yum install httpd -y"
					sh "cp -r index.html /var/www/html/"
				        sh "chmod -R 777 /var/www/html/index.html"
			}
		
		}
		
		stage ("start"){
			agent {
		
				label "slave-1"
				customWorkspace "/mnt/jenkin-slave1"
		
		}
		steps {
				sh "service httpd start"
		
		}
		
		}

}

}
