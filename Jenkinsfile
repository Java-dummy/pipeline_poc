pipeline { 
    agent any  
	stages {
			stage('compile') {
				steps {
					bat 'mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
					   }
				}
			}
}
