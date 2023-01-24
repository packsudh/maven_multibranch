@Library('newlibrary')_
pipeline
{
    agent any
    stages
        {
            stage ("Continuous Download_Loans")
            {
                steps
                {
                    script
                    {
                        cicd.newGit("https://github.com/packsudh/MavenNew.git")
                    }
                }
            }
        
            stage ('Continuous Build_Loans')
             {
                steps
                {
                    script
                    {
                        cicd.newMaven()
                    }
                }
            }
           
            
      }
}
