def print_script
masterBuild {
  sh 'ls'

  print_script = load 'print.groovy'
}

node{

  
  stage('Print'){
    print_script.print_hello()
  }


}

