node {
	def app
        stage('clone') { 
		checkout scm

        }
        stage('build') { 
                app = docker.build("xavki/nginx")
        }
        stage('run') { 
                docker.image('xavki/ngnix').withRun('-p 80:80' {c ->
		sh 'docker ps'
		sh 'curl localhost'
		}
        }
}
