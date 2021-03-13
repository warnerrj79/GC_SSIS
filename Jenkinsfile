node{
  stage('Clone') {
    def clonedir = "C:\\1_Clones"
    if (fileExists("${clonedir}")) {
      echo "Clone Directory Exists"
    } else {
      new File("${clonedir}").mkdir()
    }
    
    def numberclonedir = "${clonedir}\\Rob_${env.BUILD_NUMBER}"
    new File("${numberclonedir}").mkdir()
    
    dir("${numberclonedir}") {
      echo "Working Directory is: ${pwd()}"
      checkout scm
    }
    
    
  }
  stage('Build') {
    def builddir = "C:\\2_Builds"
    if (fileExists("${builddir}")) {
      echo "Build Directory Exists"
    } else {
      new File("${builddir}").mkdir()
    }
    
    def numberbuilddir = "${builddir}\\Rob_${env.BUILD_NUMBER}"
    new File("${numberbuilddir}").mkdir()
    
    dir("${numberclonedir}") {
      bat "cd"
    }
    
    //dir("${numberbuilddir}") {
      //echo "Working Directory is: ${pwd()}"
      //bat "cd"
      //echo bat "devenv.com \"${numberclonedir}\"  "
      
  //}

    
  }

    
}
