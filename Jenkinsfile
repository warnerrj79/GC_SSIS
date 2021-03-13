node{
  stage('Clone') {
    echo "${env.BUILD_NUMBER}"
    
    newdir = new File("C:\\Rob_${env.BUILD_NUMBER}").mkdir()
    echo newdir
    
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
