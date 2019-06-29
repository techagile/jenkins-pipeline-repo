pipeline {
	agent any
	// This shows a simple build wrapper example, using the AnsiColor plugin.
	node {
	    // This displays colors using the 'xterm' ansi color map.
	    ansiColor('xterm') {
	        // Just some echoes to show the ANSI color.
	        stage "\u001B[31mI'm Red\u001B[0m Now not"
	    }
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