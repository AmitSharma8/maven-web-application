pipeline {
 //  agent any     //job will run on any agent which is available
 //  agent { label 'slave1' }    //job will run only on agent having tag 'slave1'
 //  agent { label 'docker && slave1'}
     agent {label 'docker || slave1'}
     triggers { pollSCM('* * * * *') }
     stages {
       stage('Build') {steps {echo 'Building is done'}}
       stage('Test') {steps {echo 'Testing is done'}}
       stage('Deploy') {steps {echo 'Deployment is done'}}
       stage('email') {steps {echo 'mail sent'}}
    }
}
