node{
  def clonedir = "C:\\1_Clones"
    if (fileExists("${clonedir}")) {
      echo "Clone Directory Exists"
    } else {
      new File("${clonedir}").mkdir()
    }
  
  def numberclonedir = "${clonedir}\\Rob_${env.BUILD_NUMBER}"
  
  def builddir = "C:\\2_Builds"
    if (fileExists("${builddir}")) {
      echo "Build Directory Exists"
    } else {
      new File("${builddir}").mkdir()
    }
    
    def numberbuilddir = "${builddir}\\Rob_${env.BUILD_NUMBER}"
  
  
  
  
  stage('Clone') {
    new File("${numberclonedir}").mkdir()
    
    dir("${numberclonedir}") {
      echo "Working Directory is: ${pwd()}"
      checkout scm
    }
  }
  stage('Build') {
    
    new File("${numberbuilddir}").mkdir()
    
    dir("${numberclonedir}") {
      bat "cd"
      bat "echo %PATH%"
      //bat "devenv.com \".\\GC_Test\\GC_Test.sln\""
    }
    
    //dir("${numberbuilddir}") {
      //echo "Working Directory is: ${pwd()}"
      //bat "cd"
      //echo bat "devenv.com \"${numberclonedir}\"  "
      
  //}

    
  }

    
}
