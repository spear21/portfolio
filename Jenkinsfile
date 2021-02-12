node {
    stage('Cloning Git') {
        git branch: 'master', url: 'https://github.com/spear21/portfolio.git'
    }
    stage('Install modules') {
         sh 'npm install'
    }
    stage('Test') {
        sh 'npm test'
    }
    stage('Build') {
        sh 'npm run build --prod'
    }
    stage('Copy') {
    'cp -a /var/lib/jenkins/workspace/portfolio pipeline/dist/portfolio/. /var/www/portfolio pipeline/html/'
    }
}