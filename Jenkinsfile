pipeline { 
tools { 
 jdk 'my_jdk' 
 maven 'my_maven' 
} 
agent none 
stages { 
	stage('checkout')
	{ 
		agent any 
		steps { git 'https://github.com/nelavigi/jenkins_training.git' } 
	} 
	stage('compile')
	{ 
		agent any 
		steps{ sh 'mvn compile' } 
	} 
	stage('unitTest')
	{ 
		agent any 
		steps{ sh 'mvn test' } 
	} 
} 
}
