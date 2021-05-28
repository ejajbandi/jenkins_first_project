pipeline {

  agent { label 'myfirstproject' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/ejajbandi/jenkins_first_project.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "mynginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
