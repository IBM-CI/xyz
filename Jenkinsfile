pipeline {
  agent any
stages {
stage('Compile Stage') {
steps {
withMaven(maven : 'maven'){
  sh 'mvn compile'
    }
  }
}
stage('Testing Stage') {
steps {
withMaven(maven : 'maven'){
  sh 'mvn Test'
    }
  }
}
stage('Deployment Stage') {
steps {
withMaven(maven : 'maven'){
  sh 'mvn deploy '
    }
  }
}
}

}
