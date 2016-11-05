node{
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    bat "set"
    step([$class: 'GitHubPRCommentPublisher', comment: [content: 'test comment']])
  }
}
