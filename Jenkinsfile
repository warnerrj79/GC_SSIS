node{
  stage('Clone') {
    def newclonedir = "C:\\1_Clones"
    if (fileExists("newbuilddir")) {
      new File(newbuilddir).mkdir()
    }
    
    def newdir = "${newclonedir}\\Rob_${env.BUILD_NUMBER}"
    new File(newdir).mkdir()
    echo "Working Directory is: ${pwd()}"
    
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
