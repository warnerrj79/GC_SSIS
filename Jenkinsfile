node{
  stage('Clone') {
    def newdir = "C:\\Rob_${env.BUILD_NUMBER}"
    new File(newdir).mkdir()
    echo "Working Directory is: ${pwd()}"
    
    dir("newdir")
    
    echo "Working Directory is: ${pwd()}"
    
    checkout scm
    
    
  }
  stage('Build') {

    
    echo "Hey!"
    echo "Directory is ${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_COMMITTER_NAME}"
  }
    
}
