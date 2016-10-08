node{

  stage('Checkout'){
    checkout scm
    

    def gitCommit = sh script: 'git rev-parse HEAD', returnStatus: true
    echo gitCommit
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}
