pipeline {
	agent any
	environment{
		DOCKER_TAG = getDOCKERTAG()
	}
	stages{
		stage('Build Docker Image')
		{
			steps{
				sh "docker bild . -t kammana/nodeapp:${DOCKER_TAG}"
			}
		}
	}
	
}
def getDockerTag(){
	def tag = sh script: 'git rev-parse HEAD', returnStdout:true
	return tag
}
