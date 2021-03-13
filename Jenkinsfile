node{
  stage('Clone') {
    new File('C:\Rob').mkdir()
    dir ('C:\Rob')
    
    checkout scm
    
    
  }
  stage('Build') {

    
    echo "Hey!"
    echo "Directory is ${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_COMMITTER_NAME}"
  }
    
}
