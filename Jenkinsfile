pipeline 
{
  agent any
  stages
  {
    stage('Build')
    {
      steps
      {
        sh 'cd main && g++ -o a pipeline.cpp'
        build 'PES1UG20CS570-1'
        echo 'Build stage successful'
      }
    }
    stage('Test')
    {
      steps
      {
        sh 'cd main && ./a'
        echo 'test stage successful'
      }
    }
  }
    post
    {
      failure
      {
        echo 'pipeline failed'
      }
    }
  }
