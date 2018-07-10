pipeline {
  agent any
stages {
stage('Compile Stage') {
steps {
withMaven(maven : 'maven',
          mavenSettingsConfig: 'my-maven-settings',
        mavenLocalRepo: '.repository'){
  sh 'mvn clean install'
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
