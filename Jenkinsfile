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
  
  
  
  //////////////////////////////////////////////////////////////////
    
  
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
      bat "\"C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\Community\\Common7\\IDE\\devenv.com\" \".\\GC_Test\\GC_Test.sln\" /rebuild"
    }
    
    dir ("${numberclonedir}\\GC_Test\\bin\\Development") {
      bat "copy GC_Test.ispac ${numberbuilddir}"
    }
  }
  
  stage('Copy S3') {
    bat "\"C:\\Program Files\\Amazon\\AWSCLIV2\\aws.exe s3 cp GC_Test.ispac s3://gctestssis/Test/\""
  }

    
}
