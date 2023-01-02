pipeline{
  agent any
  tools{
      maven "Maven3.6.0"
  }
  stages{
    stage('1GetCode'){
        steps{
        sh "echo 'cloning the latest application version'"
        git branch: 'feature', credentialsId: 'gitHubCredentials', url: 'https://github.com/OyinAA/maven-web-application.git'
        }
    }
    
    stage('2Test&Build'){
        steps{
            sh "echo 'running JUnit-test-cases'"
            sh "echo 'testing must pass to create artifacts'"
            sh "mvn clean package"
        }
    }
    /*
    stage('3CodeQuality'){
        steps{
           sh "echo 'Perfoming CodeQualityAnalysis'"
           sh "mvn sonar:sonar"
        }
    }
    stage('4uploadNexus'){
        steps{
           sh "mvn deploy"
        }
    }
    stage('5deploy2prod'){
        steps{
           deploy adapters: [tomcat9(credentialsId: 'tomcat-credentials', path: '', url: 'http://3.84.154.167:8177/')], contextPath: null, war: 'target/*war' 
        }
    }
  }
  post {
      always{emailext body: '''Hey guys
Please check build status.

Thanks,
April Tech
+ 1 470 461 1733''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'Fintech-app@gmail.com'}
      success{emailext body: '''Hey guys
Good job build and deployment is successful.

Thanks,
April Tech
+ 1 470 461 1733''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'Fintech-app@gmail.com'}
      failure{emailext body: '''Hey guys
Build failed please go back to the source code and fix issues.

Thanks,
April Tech
+ 1 470 461 1733''', recipientProviders: [buildUser(), developers()], subject: 'Success', to: 'Fintech-app@gmail.com'}
  }
  */
}
}
