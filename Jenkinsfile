node {
    stage('Cloning Git') {
      steps {
        git branch: 'master', url: 'https://github.com/spear21/portfolio.git'
      }
    }
    stage('Install modules') {
       steps {
         sh 'npm install'
       }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build --prod'
      }
    }
    stage('Copy') {
      steps {
        sh 'cp -a /var/lib/jenkins/workspace/portfolio pipeline/dist/portfolio/. /var/www/portfolio pipeline/html/'
      }
    }
}