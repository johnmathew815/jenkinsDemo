pipeline
{
	agent any
	stages {
	
	 stage('BUILD APPLICATION'){
	 steps{
	 bat 'mvn clean install'
	 }
	 }
	 
	 stage('DEPLOY APPLICATION TO MULE CLOUDHUB'){
	 steps{
	 bat 'mvn clean package deploy -Dusername=jmp110496 -Dpassword=Fathima000@ -Denvironment=Sandbox -Dworkers=1 -DworkerType=Micro -DapplicationName=mule-maven-plugin-demo -DmuleDeploy'
	 }
	 }
	 
	 stage('PERFORM REGRESSION TESTING'){
	 
	 steps{
	 bat 'newman run C:\\Users\\John\\Desktop\\muleMavenCollection.postman_collection.json --disable-unicode'
	 }
	 }
	 
	}

}
