pipeline
{
  agent any
  stages
  {
    stage ('Login to AWS')
    {
        steps
       {
          withAWS(credentials: 'CreateCFT', role: 'arn:aws:iam::611373030319:role/JenkinsAccessCF, region: 'us-east-1')
          {
            sh 'aws configure list'
            sh 'aws cloudformation create-stack --stack-name EC2InstCreationstack --template-body file://EC2InstCFT.json'
          }  
       }
    }
  }
}
