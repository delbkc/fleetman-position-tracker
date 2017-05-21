node {
   stage('Preparation') { 
      git 'https://github.com/delbkc/fleetman-position-tracker'
   }
   stage('Build') {
     sh "mvn package"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
