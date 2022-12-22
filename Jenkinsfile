pipeline {
agent{
label{
		label "built-in"
		customWorkspace "/mnt/myproject"
}
}

stages {

		stage ("deploy-1"){
			steps {
				        sh "yum install httpd -y"
					sh "cp index.html /var/www/html/index.html"
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
