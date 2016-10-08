node{
  
  git_sha = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
  
  stage('Checkout'){
    print git_sha
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}
