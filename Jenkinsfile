pipeline {
      agent none
      stages{
          stage('Checkout') {
               agent {
                label "master"
               }
               steps {
                  echo "Compiled Successfully!!";
                 }
               }
          stage('Compile') {
               agent {
                label "Windows_Node"
               }
               steps {
                  echo "Compiled Successfully!!";
                 }
               }
           stage('JUnit') {
               agent {
                label "master"
               }
               steps {
                  echo "Junit passes successfully!!";
                 }
               }
           stage('Quality-Gate') {
               agent {
                label "Windows_Node"
               }
               steps {
                  echo "Quality-Gate passed successfully!!";
                 }
               }
           stage('Deploy') {
               agent {
                label "master"
               }
               steps {
                  echo "Pass!!";
                 }
               }
          } 
   post {
       always {
           echo "this will always run "
          }
       success{
           echo "this will run only when it is successful "
          }
       failure{
           echo "this will run only if fails "
          }
      unstable{
           echo "this will only when the run is marked as instable "
          }
      changed{
           echo "this will run only if the state of the pipeline has changed for example if the pipeline was previously failing but now successful "
          }
      }
}
