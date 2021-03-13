node{
  stage('Clone') {
    echo "${pwd()}"
    def newdir = "C:\\Rob_${env.BUILD_NUMBER}"
    new File(newdir).mkdir()
    echo "${pwd()}"
    dir(newdir)
    
    checkout scm
    
    
  }
  stage('Build') {

    
    echo "Hey!"
    echo "Directory is ${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_COMMITTER_NAME}"
  }
    
}
