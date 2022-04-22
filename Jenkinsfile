pipeline {
 agent any
  stages {
    stage("git") {
      steps {
        sh 'echo "Check out GitHub"'
        git branch: 'main', url: 'https://github.com/dprzegal/website3.git'
      }
    }
    stage("deploy") {
      steps {
        sh 'echo "Deploy to Nginx webserver"'
        sh 'rsync -avh /var/lib/jenkins/workspace/pipelineManualApproval3/* /var/www/website/'
      }
    }
  }
}
