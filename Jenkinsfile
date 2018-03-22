pipeline { 
    agent any  
		stages {
			stage('compile') {
				steps {
					bat 'C:\Program Files\apache-maven-3.5.3\bin\mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
					   }
				}
			}
}
