// Declarative pipeline
// we don't need node,

pipeline {
	// agent any // It is similar to node, where your build is going to run and it will give lot of flexibility
	
	//running the build in the docker agent
	agent {	docker {	image 'maven:3.6.3'} }   
	
	// In declarative pipeline, we should keep the tasks in stage, and stages are compulsory
	stages {
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"
				echo "Boshanam Stage"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	}	
	post{
		always{
			echo "I will always execute"
		}
		success{
			echo "I will execute when step of pipeline is succeeded"
		}
		failure{
			echo "I will execute when any of the step failed"
		}
		changed{
			echo "I will execute when the status of the build changed from the previous build"
		}
	 }
	}

	



// Comments
//scripted pipeline
// node is the machine where we want to run the pipeline
// stage - stages in the pipeline 
// stage blocks are optional


// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// 	stage('Integration Test2') {
// 		echo "Integration Test2"
// 	}
// }

// node {
// 	echo "Build"
// 	echo  "Test"
// 	echo  "Integration Test"
// 	echo  "Integration Test2"
// }


