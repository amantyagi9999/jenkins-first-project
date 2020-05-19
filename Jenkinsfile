//scripted
/*node{
		echo "Build"
		echo "Test"
		echo "Integration Test"	
} */

//declarative

pipeline{
	//agent any
	agent{ docker{ image 'maven:3.6.3'} }
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"	
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
			echo "Run Always !"
		}
		success{
			echo "Run when success!"
		}
		failure{
			echo "Run when fail!"
		}
	}
}