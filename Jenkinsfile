pipeline{

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/master6789/playjenkins.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
