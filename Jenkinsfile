pipeline{

agent any
parameters{
    string(name: 'UserId', defaultValue:'',
            description: 'Enter your user ID')} 
stages {
  stage('Login'){
    steps{echo "Active User is ${UserId}"}}
  stage ('first stage'){
   steps{echo 'Hello'
         input 'continue to next stage?'}
    }
   
  stage ('Second stage'){
   steps{echo 'world'}}
}
}
      
