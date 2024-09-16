pipeline{
  agent any 
  tools {
    maven "maven3.9.9"
  }  
  stages {
    stage('1GetCode'){
      steps{
        sh "echo 'cloning the latest application version' "
        git credentialsId: 'tomcat-credentials_updated', url: 'https://github.com/folakunle1/maven-web-application'
      }
  }
    stage('3Test+Build'){
      steps{
        sh "echo 'running JUnit-test-cases' "
        sh "echo 'testing must passed to create artifacts ' "
        sh "mvn clean package"
      }
    }
    /*
     stage('4CodeQuality'){
     steps{
     sh "echo 'Perfoming CodeQualityAnalysis' "
     sh "mvn sonar:sonar"
      }
    }
     stage('5uploadNexus'){
     steps{
     sh "mvn deploy"
      }
    } 
     stage('8deploy2prod'){
     steps{
     deploy adapters: [tomcat9(credentialsId: 'tomcat-credentials_updated', path: '', url: 'http://13.52.249.148:8080/')], contextPath: null, war: 'target/*war' }
    }     
  }
  
  post{
    always{
      emailext body: '''Hey guys
Please check build status.

Thanks.
Obi Tech
+1 705 001 2010''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'kunlefree4christ@gmail.com'
    }
    success{
      emailext body: '''Hey guys
Good job build and deployment is successful.

Thanks.
Obi Tech
+1 705 001 2010''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'kunlefree4christ@gmail.com'
    } 
    failure{
      emailext body: '''Hey guys
Build failed. Please resolve issues.

Thanks.
Obi Tech
+1 705 001 2010''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'kunlefree4christ@gmail.com'
    }
   }
   */
 }
}
