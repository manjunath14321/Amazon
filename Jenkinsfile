pipeline {
    agent 
       label 'dev'
    
    stages {

        stage('pull') {
            steps {
                git branch: 'master', url: 'https://github.com/manjunath14321/Amazon.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

        
    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
