pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        git(url: 'https://github.com/jonathanelbailey/create_ovirt_iso.git', branch: 'master', poll: true, credentialsId: '7416e6fd-dfed-46ab-b1a2-3f52e719fdf7')
      }
    }
  }
}