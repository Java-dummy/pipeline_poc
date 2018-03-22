pipeline { 
    agent any  
	environment {
    PATH = "C:\Program Files\apache-maven-3.5.3\bin:$PATH"
  }
		stages {
			stage('compile') {
				steps {
					bat 'mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
					   }
				}
			}
}
