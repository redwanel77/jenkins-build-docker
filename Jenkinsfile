node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("nginx")
    }

    stage('Run image') {
        docker.image('nginx').withRun('-p 70:80') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }

    }
    
}

