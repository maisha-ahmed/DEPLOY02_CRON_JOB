pipeline 
{
    agent any 
    //triggers
    //{
    //   cron('*/10 * * * *')
    //}
    stages 
   {
        stage('Build') 
        {
            steps 
            {
                echo 'Hello world!' 
            }
        }
        stage('Test')
        {
           steps  
           {
             echo 'Hello KuraLabs!'
           }
        }
        stage('Deployment')
        {
           steps
           {
              echo 'Goodbye World!'
           }
        }
    }
    post
    {
      success 
        {          
            triggers
            {
               cron('41 20 * * *')
            }  
            httpRequest = "https://ec2.amazonaws.com/?Action=StopInstances
                           &InstanceId.1=i-083b0c84b2888ead1
                           &AUTHPARAMS
        }
    }
}
