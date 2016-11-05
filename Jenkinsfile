node{

  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    step([$class: 'GitHubPRCommentPublisher', comment: [content: 'test comment']])
  }


}

