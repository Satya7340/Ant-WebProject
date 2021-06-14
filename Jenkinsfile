pipeline
{
agent any
stages
{
  stage('code scm checkout')
  { steps{ git branch: 'master', url: 'https://github.com/Satya7340/Ant-WebProject'}
  }
  
  stage('prepare the environment')
  { steps{
    withAnt(installation: 'myant', jdk: 'my_Java') 
      { sh 'ant init'}
   }
  }
  
 }

}
