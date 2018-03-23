pipeline { 
    agent any  
	stages {
			stage('compile') {
				steps {
					step {
					def mvn_version = 'M3'
					withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] )
					bat 'mvn clean cobertura:cobertura -Dcobertura.report.format=xm'
					}
					   }
				}
			}
}
