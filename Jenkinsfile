node{

  stage('Checkout'){
    checkout scm
    
    gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
    echo gitCommit
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}
