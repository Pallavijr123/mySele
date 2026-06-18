pipeline{
	agent any
	
	tools{
	maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/Pallavijr123/mySele.git'
			}
		}
		stage('Compile'){
			steps{
				sh 'mvn compile'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
			}
		}
	}
}
