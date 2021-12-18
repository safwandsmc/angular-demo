pipeline {
  agent {
    node {
      label 'Angular12'
    }

  }
  stages {
    stage('Install Packages') {
      steps {
        echo 'Install Packages'
        sh 'npm i'
        sh 'ls'
      }
    }

    stage('Build Project') {
      steps {
        echo 'Build'
        sh 'ng build'
        sh 'ls'
      }
    }

    stage('Is Deploy?') {
      steps {
        input(message: 'Is Deploye?', ok: 'OK')
      }
    }

    stage('Publish') {
      steps {
        echo 'Publish files'
        sh 'sshpass -p "Admin@#321" scp ./dist Administrator@192.168.192.12:C:\\test'
      }
    }

  }
}
