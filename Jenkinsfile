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
withMaven(maven : 'maven'){
  sh 'mvn clean compile'
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
