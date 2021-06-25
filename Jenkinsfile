// Powered by Infostretch 

timestamps {

node () {

	stage ('mithun-dev - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/development']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '30de2c62-5afb-48c0-b5b8-5502660bbeec', url: 'https://github.com/mahaboobbasha1/maven-web-application.git']]]) 
	}
	stage ('mithun-dev - Build') {
 			// Maven build step
	withMaven(maven: 'maven3.8.1') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		} 
	}
}
}