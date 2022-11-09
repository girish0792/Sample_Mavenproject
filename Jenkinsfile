pipeline {
    agent any
    stages {
	stage('downloading from git') 
      { git https://github.com/girish0792/Sample_Mavenproject.git
        }

        stage ('Build Servlet Project') {            
	steps {
                sh  'mvn clean package'
            }

            post{
                success{
                    echo 'Now Archiving ....'

                    archiveArtifacts artifacts : '**/*.war'
                }
            }
        }
    }
}
