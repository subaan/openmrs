node {

    environment {
        PATH = '$PATH:/home/appranix/.rvm/gems/ruby-2.2.4/bin/prana'
    } 
   stage('Build') {
         git 'https://github.com/subaan/openmrs.git/'
         sh 'mvn package'
   }

stage("publish to s3") {
	sh 'echo war published to s3'
}

stage('Initiate prana deployment') {


       sh 'echo successfully logged in prana'

       sh 'echo organization is set as devorg'

       sh 'echo assembly is set as shopping-cart'

       sh 'echo Transition variable update build ver'

       sh 'echo Transition variable update build ver'

       sh 'echo deployement is started'
      
   }
}
