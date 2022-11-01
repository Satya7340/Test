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
  stage('Input'){
           steps{ 
               script{
                   def resp = input message: 'Hi There',
                       parameters: [string(defaultValue: '', description 'Enter Response 1', name: 'RESPONSE1'),
                                    string(defaultValue: '', description 'Enter Response 2', name: 'RESPONSE2')]
                   echo "${resp.RESPONSE1} + ${resp.RESPONSE2}"
               }   } }
    }
   
  stage ('Second stage'){
   steps{echo 'world'}}
}
}
      
