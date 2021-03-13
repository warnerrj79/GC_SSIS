node{
  stage('Clone') {
    def newclonedir = "C:\\1_Clones"
    if (fileExists("newclonedir")) {
      new File(newcloneddir).mkdir()
    }
    
    def newdir = "${newclonedir}\\Rob_${env.BUILD_NUMBER}"
    new File(newdir).mkdir()
    
    dir("${newdir}") {
      echo "Working Directory is: ${pwd()}"
      checkout scm
    }
    
    
  }
  stage('Build') {
    def newbuilddir = "C:\\2_Builds"
    if (fileExists("newbuilddir")) {
      new File(newbuilddir).mkdir()
    }

    
  }
    
}
