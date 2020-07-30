pipeline {
	agent any
	stages {
		stage('checkout') {
	steps {
	checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/sunilvirat/exa.git']]])
	}
stage('ls') {
	steps {
	    sh label: '', script: 'ls'
	}
}
stage('apply docker file'){
agent {
                        label "docker"
                    }
steps{
    sh label: '', script: '''scp fi.sh dockerswarm@172.31.33.211:/home/dockerswarm/workspace/se/'''
}
}
}
}
