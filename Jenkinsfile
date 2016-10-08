node{

  try{
    stage('Checkout'){
      updateGitHubStatus("Checkout", "pending")
      checkout scm
      updateGitHubStatus("Checkout", "success")
    }
  }
  catch(err){
    updateGitHubStatus("Checkout", "failure")
  }
  
  stage('Print'){
    echo 'Hello!'
  }

  stage('Sonar'){
    step([$class: 'SonarRunnerBuilder'])
  }
}

def updateGitHubStatus(context, status){
  def gitCommit = bat 'git rev-parse HEAD'
  bat 'curl --user mchen404 https://api.github.com/repos/mchen404/jenkins_pipline/statuses/$(gitCommit) -H "Content-Type: application/json" -X POST -d "{\"state\": $(status), \"context\": \"$(context) \"description\": \"Jenkins\"}"'
}
