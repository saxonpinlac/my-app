node{
    stage('SCM Code'){
      git 'https://github.com/saxonpinlac/my-app'
    }
    stage('Compile Package'){
      def mv_var = tool name: 'maven', type: 'maven'
        sh "${mv_var}/bin/mvn package"
    }
    stage('SonarQube Analysis') {
        def mvnHome =  tool name: 'maven-3', type: 'maven'
        withSonarQubeEnv('sonarqube') { 
          sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
    
}
