node{
  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    sonarScanner()
  }
}
