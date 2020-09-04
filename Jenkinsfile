node {
	stage('SCM Checkout'){
		git 'https://github.com/StephanBosS4S/my-app'
	}
	stage('Compile-Package'){
	// get maven home path
	def mvnHome = tool name: 'maven3', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
	}
	      
}

