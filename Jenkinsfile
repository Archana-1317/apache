pipeline {
    
    agent any


    tools {
    jdk 'java11'
    maven 'maven'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'master',
               url: 'https://github.com/Archana-1317/apache.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://demo1013
                  '''

            }
        }
      }
     }
