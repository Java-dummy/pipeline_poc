pipeline { 
    agent any  
	stages {
		stage ('compile') {
			steps {
				withMaven(maven : 'Maven3.5.3') {
				bat 'mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
				}
			    }
			}
	}
}
