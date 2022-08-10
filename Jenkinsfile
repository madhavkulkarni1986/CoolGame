pipeline {
    agent { dockerfile true }
    stages {
        stage('Clone') {
            steps {
		script {
           		git credentialsId: 'jenkins-user-github', url: 'https://github.com/madhavkulkarni1986/coolGame.git'
          	}
            }
        }
	stage('Build') {
	   steps {
		sh 'mkdir build && cd build'
		sh 'cmake ..'
	   }
	}
	stage('Test') {
	   steps {
		sh 'cd ${WORKSPACE}/build'
		sh 'echo "Running tests..."'
		sh 'echo "===================="'
		sh 'ctest -VV'
	   }
	}
    }
}
