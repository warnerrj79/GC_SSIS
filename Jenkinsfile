node{
  stage('Clone') {
    echo "${env.BUILD_NUMBER}"
    
    new File("C:\\Rob_${env.BUILD_NUMBER}").mkdir()
    dir('C:\\Rob2')
    
    checkout scm
    
    
  }
  stage('Build') {

    
    echo "Hey!"
    echo "Directory is ${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_CHECKOUT_DIR}"
    echo "${env.GIT_COMMITTER_NAME}"
  }
    
}
