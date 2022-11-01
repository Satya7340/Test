pipeline{

agent any
parameters{
    string(name: 'UserId', defaultValue:'',
            description: 'Enter your user ID')} 
stages {
  stage('Login'){
       steps{echo "Active User is ${UserId}"}}
  stage ('first stage'){
      steps{echo 'Hello ${UserID}'
             input 'continue to next stage?'}}
  stage('Input'){
           steps{ 
               script{
                   def resp = input message: 'Hi There',
                       parameters: [string(defaultValue: '', description: 'Enter Response 1', name: 'RESPONSE1'),
                                    string(defaultValue: '', description: 'Enter Response 2', name: 'RESPONSE2')]
                   echo "${resp.RESPONSE1} by ${resp.RESPONSE2}"
               }   } }
   
  stage('Input'){
           steps{ 
               script{
                   env.RESP1 = input message: 'Please provide environment details',
                       parameters: [string(defaultValue: '', description: 'Enter Response 1', name: 'RESPONSE1')]
                   env.RESP2 = input message: 'Please provide environment details',
                       parameters: [string(defaultValue: '', description: 'Enter Response 2', name: 'RESPONSE2')]
                   echo "${env.RESPONSE1} deployment is complete"
               }   } }  
  stage ('Second stage'){
   steps{echo "${env.RESPONSE2} deployment is next"}}
}
}
      
