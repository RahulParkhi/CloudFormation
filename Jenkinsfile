pipeline
{
  agent any
  stages
  {
    stage ('Login to AWS')
    {
        steps
       {
          withAWS(credentials: 'CreateCFT', region: 'us-east-1') {
            sh 'aws configure list'
        }  
    }
    stage ('submit cloud formation template')
    {
        steps
        {
          //sh 'aws cloudformation create-stack --stack-name EC2InstCreationstack --template-body file://EC2InstCFT.json --region "us-east-1"'
          sh 'aws configure list'
        }
    }
  }
}
