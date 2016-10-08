node{

  stage('Checkout'){
    checkout scm
    

    def gitCommit = bat 'git rev-parse HEAD'
    echo gitCommit
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}
