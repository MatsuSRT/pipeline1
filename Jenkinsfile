node {
  def app

  stage('Clone the repository'){
    checkout scm
  }

  stage('Build image'){
    app = docker.build("matsu365/pipeline1")
  }

  stage('push'){
    docker.withRegistry('https://registry.hub.docker.com','docker-hub-credentials'){
      app.push("latest")
    }
  }
}
