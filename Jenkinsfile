pipeline {

    agent any
   parameters {
  choice choices: ['DeployL1_L2_L3', 'L4', 'L6'], description: 'Please select the environment to Deploy!!!', name: 'ENV_NAME'
  choice choices: ['HSVALIDATION_BUSINESS_SERVICE', 'HSVALIDATION_DATA_SERVICE'], description: 'Please select the application!!!', name: 'APP_NAME'
}
 stages {

        stage('Code checkout') {
             when {
                  expression { params.ENV_NAME =='DeployL1_L2_L3'}
                  }
             steps {
                    echo "helllo"
               }
        }
     
     stage('Code checkout') {
             when {
                  expression { params.ENV_NAME =='DeployL1_L2_L3'}
                  }
             steps {
                 scripts{
                 sh '''
                 docker build -t testimage .
                 docker run --name=newcontainer-d -p 9898:8080 testimage
                 '''
                 }
               }
        }
        
        }
 }
