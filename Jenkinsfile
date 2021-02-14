pipeline {
  agent any
  tools { 
        maven 'maven-3.6.3' 
        jdk 'jdk8' 
  }
  stages {
    stage ('Initialize path') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
       }
    }
    stage('Install Dependencies On local Cache') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}
