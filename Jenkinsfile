@Library('newlibrary')_
pipeline
{
    agent any
    stages
        {
            stage ("Continuous Download_Master")
            {
                steps
                {
                    script
                    {
                        cicd.newGit("https://github.com/packsudh/MavenNew.git")
                    }
                }
            }
        
            stage ('Continuous Build_Master')
             {
                steps
                {
                    script
                    {
                        cicd.newMaven()
                    }
                }
            }
           stage ('Continuous Deployment_Master')
            {
                steps
                {
                    script
                    {
                        cicd.newDeploy("DeclarativePipelineWithSharedLibraries","172.31.17.13","test1")
                    }
                }
            }
            
            stage ('Continuous Testing_Master')
            {
                steps
                {
                    script
                    {
                        cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                        cicd.runSelenium("DeclarativePipelineWithSharedLibraries")
                    }
                }
            }
            stage ('Continuous Delivery_Master')
            {
                steps
                {
                    script
                    {
                        cicd.newDeploy("DeclarativePipelineWithSharedLibraries","172.31.12.15","prod1")
                    }
                }
            }
            
      }
}
