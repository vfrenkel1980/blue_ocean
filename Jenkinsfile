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
        bat 'mvn clean install -Dsurefire.suiteXmlFiles=testng_mobile.xml  -Dlog4j.configurationFile=src//main//resources//log4J2.xml -B'
      }
    }

  }
}