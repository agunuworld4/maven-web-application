node {
  
  def mvnHome = tool name: 'Maven04', type: 'maven'

  stage ('checkoutCode'){
  checkout([$class: 'GitSCM', branches: [[name: '*/development']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/agunuworld4/maven-web-application']]])
  }
stage ('PackageApp'){
  sh "${mvnHome}/bin/mvn clean install package"
}


}
