node{
    stage('SCM Code'){
      git 'https://github.com/javahometech/my-app'
    }
    stage('Compile Package'){
      def mv_var = tool name: 'maven', type: 'maven'
        sh "${mv_var}/bin/mvn package"
    }
}
