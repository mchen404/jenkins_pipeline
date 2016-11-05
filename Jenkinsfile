test_load = load "print.groovy"

node{

  stage('Checkout'){
    checkout scm
  }
  
  stage('Print'){
    test_load.print_hello()
  }


}

