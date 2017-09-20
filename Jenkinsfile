pipeline {
  agent any
  stages {
    stage('Create Ovirt Iso') {
      steps {
        git(url: 'https://github.com/jonathanelbailey/create_ovirt_iso.git', branch: 'master', poll: true, credentialsId: '7416e6fd-dfed-46ab-b1a2-3f52e719fdf7')
        sh '''chmod +x create_ovirt_iso
sudo ./create_ovirt_iso'''
        cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenSuccess: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true)
      }
      post {
        always {
          sh '''chmod +x cleanup_work
sudo ./cleanup_work'''
          
        }
        
      }
    }
  }
}