pipeline {
        agent none
        stages {
         
          stage("build & SonarQube Scanner") {
            agent any
            steps {
              withSonarQubeEnv('SonarQube_server') {
              sh" ${SCANNER_HOME**}**}/bin/sonar-scanner \
              -Dsonar.projectKey=raza.jenkins.project \
              -Dsonar.sources=. "
              }
            }
          }
        }
      }
