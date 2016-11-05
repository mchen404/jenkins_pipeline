node{
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    bash "env"
    step([$class: 'GitHubPRCommentPublisher', comment: [content: 'test comment']])
  }
}
