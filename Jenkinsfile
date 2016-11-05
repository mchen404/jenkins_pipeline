node{
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    echo env
    step([$class: 'GitHubPRCommentPublisher', comment: [content: 'test comment']])
  }
}
