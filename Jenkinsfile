pipeline {
	agent {
		node {
			label 'Linux'
		}
	}

	stages {
		stage ('Demo Stage') {
			steps{
				checkout([
					$class: 'GitSCM',
					branches: [[name: 'origin/master'], [name: 'origin/DEVA']],
					userRemoteConfigs: [[
						url: 'https://github.com/ankitppatel07/demo-project.git',
						credentialsId: ''
					]]
				])
			}
		}
	}
}