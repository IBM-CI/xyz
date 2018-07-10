pipeline {
  agent {
  lable "windows"
  }
  tools {
    maven 'maven'
    jdk 'JAVA_HOME'
  }
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
