
node{
  stage ('Checkout SCM'){
    git branch: 'master', url: 'git@github.com/spear21/portfolio.git'
  }
 stages {
    stage('Install') {
       sh 'npm install' 
    }

    stage('Build') {
      sh 'npm run build:port'
    }
}
 