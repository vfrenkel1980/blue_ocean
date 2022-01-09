pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/vfrenkel1980/aleksey.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install -Dsurefire.suiteXmlFiles=%tsng.xml%  -Dlog4j.configurationFile=src//main//resources//log4J2.xml -B'
      }
    }

  }
}