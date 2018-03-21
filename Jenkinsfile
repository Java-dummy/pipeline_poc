pipeline { 
    agent any  
		stages {
			stage('compile') {
				steps {
					sh 'mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
					   }
				}
			}
}