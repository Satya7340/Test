pipeline{

agent any
parameters{
    string(name: 'UserId', defaultValue:'',
            description: 'Enter your user ID')} 
stages {
  stage('Login'){
       steps{echo "Active User is ${params.UserId}"}}
  stage ('first stage'){
      steps{ input 'continue to next stage?'
            echo "Hello ${params.UserID}" }}
  stage('Input'){
           steps{ 
               script{
                   def resp = input message: 'Hi There',
                       parameters: [string(defaultValue: '', description: 'Enter Response 1', name: 'RESPONSE1'),
                                    string(defaultValue: '', description: 'Enter Response 2', name: 'RESPONSE2')]
                   echo "${resp.RESPONSE1} by ${resp.RESPONSE2}"
               }   } }
   
  stage('Input2'){
           steps{ 
               script{
                   env.RESP3 = input message: 'Please provide environment details',
                       parameters: [string(defaultValue: '', description: 'Enter Response 1', name: 'RESPONSE3')]
                   env.RESP4 = input message: 'Please provide environment details',
                       parameters: [string(defaultValue: '', description: 'Enter Response 2', name: 'RESPONSE4')]
                   echo "${env.RESP3} deployment is complete"
               }   } }  
  stage ('Second stage'){
   steps{echo "${env.RESP4} deployment is next"}}
}
}
      
