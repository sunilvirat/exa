pipeline {
	agent any
	stages {
stage('checkout') {
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
