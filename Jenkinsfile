// Powered by Infostretch 

timestamps {

node () {

	stage ('EBI_Online - Extranet - Mock - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '$GIT_BRANCH']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'radmar2002', url: 'https://github.com/radmar2002/maven-project.git']]]) 
	}
	stage ('EBI_Online - Extranet - Mock - Build') {
 	
// Unable to convert a build step referring to "hudson.plugins.build__timeout.BuildTimeoutWrapper". Please verify and convert manually if required.
// Unable to convert a build step referring to "jenkins.plugins.nodejs.NodeJSBuildWrapper". Please verify and convert manually if required.		// Shell build step
sh """ 
echo "Hopa 1" 
 """		// Shell build step
sh """ 
echo "Hopa 2" 
 """		// Shell build step
sh """ 
echo "Hopa 3" 
 """ 
	}
	stage ('EBI_Online - Extranet - Mock - Post build actions') {
/*
Please note this is a direct conversion of post-build actions. 
It may not necessarily work/behave in the same way as post-build actions work.
A logic review is suggested.
*/
		// Mailer notification
		step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: 'mariusr@fortech.ro ', sendToIndividuals: false])
 
	}
}
}