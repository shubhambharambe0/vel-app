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
					sh "cp /root/.jenkins/workspace/test@script/98de7066481b1b3368608ddc5996649aa9170d91fd806984ed9e1c2e1c12c05b/index.html /var/www/html/"
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
