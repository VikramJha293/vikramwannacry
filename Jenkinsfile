node {
   
   stage('SCM Checkout') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/VikramJha293/vikramwannacry.git'
     
   }
   stage('Maven Build') {
    echo 'Build is started'
      withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.5.3') {
         sh 'mvn clean compile  '
      }
   }
   stage('Test Execution') {
    echo 'Test is executed' 
      withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.5.3') {
         sh 'mvn test package'
      }
   }
    stage('Archival') {
    echo 'archived to JFrog repo' 
   }
   stage('Deploy to Dev') {
    echo 'Deploy to Dev' 
   }
}
