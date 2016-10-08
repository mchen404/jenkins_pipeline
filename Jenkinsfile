node{
  
  git_sha = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
  
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}
