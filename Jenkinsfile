pipeline {
	agent {
        	docker { image 'node:7-alpine' }
    	}
	stages {
	    stage('build1') {
    		steps {
    			echo "First step"
                bat label: '', script: 'echo %date%'
    		}
	    }
	    stage('build2') {
    		steps {
    			echo "Second step"
                bat label: '', script: 'echo %date%'
    		}
	    }
	    stage('build3') {
    		steps {
    			echo "Third step"
                bat label: '', script: 'echo %date%'
    		}
	    }
	    stage('build4') {
    		steps {
                bat 'set'
            }
	    }
	}
	post{
	    always {
	        echo "this will always run"
	    }
	    success {
	        echo "in case of success, pipeline"
	    }
	    failure {
	        echo "in case of failure"
	    }
	    unstable {
	        echo "in case unstable, pipeline"
	    }
	    changed {
	        echo "in case changed, pipeline"
	    }
	}
}