pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				bat "docker pull jadyjdjady1990/sel-dok"
			}
		}
		stage("Start Grid"){
			steps{
				bat "docker-compose up -d hub chrome"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up mytest"
			}
		}
	}
	post{
		always{
			bat "docker-compose down"
		}
	}
}