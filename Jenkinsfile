
@Library('mylibrary')_
node ('built-in')
{
    stage ('ContDownload_master')
    {
        cicd.newDownload("maven1.git")
    }
    
    stage('ContBuilt_master')
    
    {
    cicd.newBuild()
    }
    
    stage('ContDeployment_master')
    
    {
      cicd.newDeploy("ScriptedPipelineWithSharedLibrary1","172.31.91.138","testapp_sharedLibrary1")   
    }
    
       stage('ContTesting_master')
    
    {
         cicd.newDownload("FunctionaTesting.git")   
         cicd.runSelenium("ScriptedPipelineWithSharedLibrary1")  
    }
    
       stage('ContDelivery_master')
    
    {
               cicd.newDeploy("ScriptedPipelineWithSharedLibrary1","172.31.82.15","prodapp_sharedLibrary1")   
    }
}
