pipeline {

    agent any
    
    environment {
        AZURE_ID = credentials('Azure_User_Id')
        AZURE_Password = credentials('Azure_Pass')
    }

    stages {

        stage('LOGGING Azure') {
            steps {
                    sh ''' 
                            ############################### shell #############################   
                            
                            az login
                            az account show
                            deployment create --name "rg1" --location "West Europe" --template-file ${WORKSPACE}/template.json --parameters ${WORKSPACE}/template.parameters.json
                            
                            
                            
                
                '''
            }
        }
    }
}
