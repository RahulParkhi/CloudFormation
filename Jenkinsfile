pipeline
{
  agent any
  stages
  {
    stage ('Login to AWS')
    {
        steps
       {
          withAWS(credentials: 'CreateCFT', region: 'us-east-1')
          {
            sh 'aws configure list'
            //CFT cmd for EC2 instance
            //sh 'aws cloudformation create-stack --stack-name EC2InstCreationstack --template-body file://EC2InstCFT.json'
            //CFT cmd for S3 bucket creation
            sh 'aws cloudformation create-stack --stack-name S3BucketCreationstack --template-body file://S3CFT.json'
          }  
       }
    }
  }
}
