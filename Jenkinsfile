CODE_CHANGES = getGitChanges()
pipeline{
  agent any
  stages{
    stage("build"){
       when {
         expressio {
           BRANCH_NAME == 'main' && CODE_CHANGES == true
         }
       }
      steps{
            echo 'building the application...'
        }
    }  
stage("test"){
   when {
         expressio {
           BRANCH_NAME == 'dev' 
         }
       }
        steps{
            echo 'testing the application...'
        }
    }  
stage("deploy"){
        steps{
            echo 'deploy the application...'
        }
    }  
  }
}
