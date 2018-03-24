// Powered by Infostretch 

timestamps {

node () {

	stage ('Test-hard - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/test']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Java_dummy', url: 'https://github.com/Java-dummy/pipeline_poc.git']]]) 
	}
	stage ('Test-hard - Build') {
 			// Shell build step
sh """ 
mvn clean cobertura:cobertura -Dcobertura.report.format=xml 
 """ 
	}
}
}