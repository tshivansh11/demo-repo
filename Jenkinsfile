pipeline 
{
  agent any
  stages 
  {
    stage('Test') 
    {
      parallel 
      {
        
        stage('Maven test') 
        {
          steps 
          {
            echo 'testing to the any test case'
            sh "mvn test"
          }
        }

        stage('maven install')
        {
          steps 
          {
            echo 'creating .war file'
            sh "mvn install"
          }
        }

      }
    }

  }
}
