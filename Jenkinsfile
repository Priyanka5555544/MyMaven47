pipeline{
	agent any
	
	tools{
		maven 'Maven'
		}
		stages{
		stage('checkout'){
			steps{
			
			git br	anch:'master',url:'https://github.com/Priyanka5555544/MyMaven47.git'
			}
			}
		stage('build'){
			steps{
			sh 'mvn clean package'
			}
			}
		stage('Test'){
		steps{
		sh 'mvn test'
		}
		}
		stage('Run Application'){
		steps{
		sh 'java -jar target/MyMaven47-1.0-SNAPSHOT.jar'
		}}
		}
post{
success{
	echo 'build is sucessful'
	}
failure{
echo "build fail'
}
}
	
