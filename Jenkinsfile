node { //test
	stage('SCM Checkout'){
		git 'https://github.com/StephanBosS4S/my-app'
	}
	stage('Compile-Package'){
	// get maven home path
	def mvnHome = tool name: 'maven3', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
	}
	

      stage('unittests'){
      steps{
      sh 'mvn test'
    }}
     stage('mutation tests'){
      steps{
       sh 'mvn org.pitest:pitest-maven:mutationCoverage' 
 
     }
        post{
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }    
}}
}

	      
}

