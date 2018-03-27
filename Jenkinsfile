pipeline { 
    agent any  
	stages {
		stage ('compile') {
			steps {
				withMaven(maven : 'Maven3.5.3') {
				bat 'mvn clean install'
				}
			    }
			}
		
		stage ('Coverage') {
			steps {
				withMaven(maven : 'Maven3.5.3') {
				bat 'mvn clean cobertura:cobertura -Dcobertura.report.format=xml'
				junit 'single-module/target/surefire-reports/TEST*.xml'
				step([$class: 'CoberturaPublisher', autoUpdateHealth: false, autoUpdateStability: false, coberturaReportFile: 'single-module/target/site/cobertura/coverage.xml', failUnhealthy: false, failUnstable: false, maxNumberOfBuilds: 0, onlyStable: false, sourceEncoding: 'ASCII', zoomCoverageChart: false])
				}
			    }
			}
		stage ('Sonar') {
			steps {
				withMaven(maven : 'Maven3.5.3') {
				bat 'mvn package sonar:sonar -Dsonar.login=ee9d33d16c94feac8977ef6f8798e769a35c63ab -Dsonar.host.url=https://sonarcloud.io'
				}
			    }
			}
	}
}
