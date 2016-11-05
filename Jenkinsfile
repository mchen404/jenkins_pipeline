node{
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'GitHubPRCommentPublisher', comment: [content: 'test comment']])
  }
}
