node{
  stage('Clone') {
    def clonedir = "C:\\1_Clones"
    if (fileExists("${clonedir}")) {
      echo "Clone Directory Exists"
    } else {
      new File("${cloneddir}").mkdir()
    }
    
    def numberclonedir = "${clonedir}\\Rob_${env.BUILD_NUMBER}"
    new File("${numberclonedir}").mkdir()
    
    dir("${numberclonedir}") {
      echo "Working Directory is: ${pwd()}"
      checkout scm
    }
    
    
  }

    
}
