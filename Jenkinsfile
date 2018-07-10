pipeline {
agent any
stages {
stage('Compile Stage') {
steps {
withMaven(Maven : 'maven'){
  sh 'mvn clean compile'
    }
  }
}
stage('Testing Stage') {
steps {
withMaven(Maven : 'maven'){
  sh 'mvn Test'
    }
  }
}
stage('Deployment Stage') {
steps {
withMaven(Maven : 'maven'){
  sh 'mvn deploy '
    }
  }
}
}

}
