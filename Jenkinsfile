pipeline {
	agent any
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
	    stage('unit test') {
    		steps {
    			echo "Unit Test"
    			bat label: '', script: 'echo %date%'
    		}
	    }
	    stage('stress test') {
    		steps {
    		echo "Stress Test"
                bat 'set'
            	}
	    }
	    stage('Deploy') {
	    	parallel {
	    		stage("run parallel Deploy1"){
	    			steps {
	    				echo "parallel Deploy1"
	    			}
	    		}
	    		stage("run parallel Deploy2"){
	    			steps {
	    				echo "parallel Deploy2"
	    			}
	    		}
	    	}
	    }
	    
	}
	post{
	    always {
	        echo "this will always run"
	        //junit 'build/reports/**/*.xml'
	    }
	    success {
	        echo "in case of success, pipeline"
	    }
	    failure {
	        echo "in case of failure, pipeline"
	        //mail to: pranav.aggwl@gmail.com, subject: 'Pipeline failed!'
	    }
	    unstable {
	        echo "in case unstable, pipeline"
	    }
	    changed {
	        echo "in case changed, pipeline"
	    }
	}
}