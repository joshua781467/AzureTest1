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
                            deployment create --name "rg1" --location "West Europe" --template-file /Users/joe/.jenkins/workspace/AzurePipeline1/template.json --parameters /Users/joe/.jenkins/workspace/AzurePipeline1/template.parameters.json
                            
                            
                            
                
                '''
            }
        }
    }
}
