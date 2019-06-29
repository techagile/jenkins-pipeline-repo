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
	    stage('build3') {
	    	parallel {
	    		stage("run parallel stage1"){
	    			steps {
	    				echo "parallel stage1"
	    			}
	    		}
	    		stage("run parallel stage2"){
	    			steps {
	    				echo "parallel stage2"
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