node('Node1U') {

        stage('GIT clone') {
            git 'https://github.com/KiranChakka/game-of-life.git'
                        }

        stage ('Build') {
	        sh label: '', script: 'mvn package'
	                   }
        stage ('Archive') {
		    archiveArtifacts 'gameoflife-web/target/*.war'
			junit 'gameoflife-web/target/surefire-reports/*xml'
			
		                  }
}
