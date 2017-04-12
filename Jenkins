node {
   stage('Preparation') { 
      git 'https://github.com/navneethproject02/fleetman-webapp'
   }
   stage('Build') {
      sh "mvn package"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.war'
   }
}
