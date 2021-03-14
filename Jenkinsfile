node{
  //Create SCM clone directory if it does not exist
  def clonedir = "C:\\1_Clones"
    if (fileExists("${clonedir}")) {
      echo "Clone Directory Exists"
    } else {
      new File("${clonedir}").mkdir()
    }
  
  //Variable for new clone folder (not created yet)
  def numberclonedir = "${clonedir}\\Rob_${env.BUILD_NUMBER}"
  
  //Create build directory if it does not exist
  def builddir = "C:\\2_Builds"
    if (fileExists("${builddir}")) {
      echo "Build Directory Exists"
    } else {
      new File("${builddir}").mkdir()
    }
    
  //Variable for new build folder (not created yet)  
  def numberbuilddir = "${builddir}\\Rob_${env.BUILD_NUMBER}"
  
  
  
  //////////////////////////////////////////////////////////////////
    
  
  stage('Clone') {
    //Create new clone version folder
    new File("${numberclonedir}").mkdir()
    
    //Go into new folder and checkout repo
    dir("${numberclonedir}") {
      echo "Working Directory is: ${pwd()}"
      checkout scm
    }
  }
  stage('Build') {
    
    //Create new build version folder
    new File("${numberbuilddir}").mkdir()
    
    //Go into checked out repo folder and build the SSIS solution
    dir("${numberclonedir}") {
      bat "cd"
      bat "\"C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\Community\\Common7\\IDE\\devenv.com\" \".\\GC_Test\\GC_Test.sln\" /rebuild"
    }
    
    //Go into the folder where the ispac is built and copy to build version folder
    dir ("${numberclonedir}\\GC_Test\\bin\\Development") {
      bat "copy GC_Test.ispac ${numberbuilddir}"
    }
  }
  
  stage('Copy S3') {
    //Copy ispac from the build version folder to S3
    bat "\"C:\\Program Files\\Amazon\\AWSCLIV2\\aws.exe\" \"s3\" \"cp\" \"${numberbuilddir}\\GC_Test.ispac\" \"s3://gctestssis/Test/\""
  }
  
    stage('Deploy Package') {
    echo "To Do"
  }

    
}
