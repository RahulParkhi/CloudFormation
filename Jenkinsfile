pipeline
{
  agent any
  stages
  {
    stage ('submit cloud formation template')
    {
      steps
      {
        sh 'aws cloudformation create-stack --stack-name EC2InstCreationstack --template-body file://EC2InstCFT.json'
      }
    }
  }
}
