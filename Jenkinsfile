pipeline {
 //  agent any     //job will run on any agent which is available
 //  agent { label 'slave1' }    //job will run only on agent having tag 'slave1'
 //  agent { label 'docker && slave1'}
     agent {label 'docker || slave1'}
     triggers { pollSCM('* * * * *') }   //job will be trigger automatically when some commits code in github
     stages {
       stage('Build') {
          steps {
             echo 'Building is done'
             echo "Running build no. ${env.BUILD_ID} on ${env.JENKINS_URL}"  // Printing build no. and Jenkins URL
         }
       }
       stage('Test') {steps {echo 'Testing is done'}}
       stage('Deploy') {steps {echo 'Deployment is done'}}
       stage('email notification') {steps {echo 'mail sent'}}
    }
}
