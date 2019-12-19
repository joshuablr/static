pipeline {
  agent any 
  stages {
    stage("Build") {
      steps {
        sh ''' echo "Hello World" '''
        sh '''  
             echo "Multiline shell steps works too"
             ls -lah
           ''' 
      }
    }
    /*
    * Added linting support for the HTML files
    * Need to install the tidy in the jenkins server
    * sudo apt install tidy
    */
    stage("Lint HTML") {
      steps {
        sh ''' tidy -q -e *.html '''
      }
    }
  }
}
