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
      { sh 'ant prepare'}
   }
  }
  
  stage('code compile')
  { steps{sh 'ant compile'
          }
  }
  
  stage('code war')
  { steps{sh 'ant war'
          }
  }
  stage('code jar')
  { steps{sh 'ant jar'
          }
  }

}

}
