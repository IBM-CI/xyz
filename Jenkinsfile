pipeline {
agent any
stages {
stage('Compile Stage') {
steps {
withMaven(Maven : 'maven_3_5_0'){
  sh 'mvn clean compile'
    }
  }
}
stage('Testing Stage') {
steps {
withMaven(Maven : 'maven_3_5_0'){
  sh 'mvn Test'
    }
  }
}
stage('Deployment Stage') {
steps {
withMaven(Maven : 'maven_3_5_0'){
  sh 'mvn deploy '
    }
  }
}
}

}
