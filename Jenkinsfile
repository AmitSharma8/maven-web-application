pipeline {
  agent { label 'slave1' }    //any=job will run any slave, 'label slave1'=job will run only on slave1
  stages {
    stage('Build') {steps {echo 'Building is done'}}
    stage('Test') {steps {echo 'Testing is done'}}
    stage('Deploy') {steps {echo 'Deployment is done'}}
    stage('email') {steps {echo 'mail sent'}}
    }
}
