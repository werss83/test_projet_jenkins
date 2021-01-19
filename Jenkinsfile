node {

stage('SCM'){
 git 'https://github.com/werss83/test_projet_jenkins'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.87:9000 -Dsonar.login=af7392a095503ba6218750b224a236f4df0c8b07"
    }
}
