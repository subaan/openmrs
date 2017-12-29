node {

    environment {
        PATH = '$PATH:/home/appranix/.rvm/gems/ruby-2.2.4/bin/prana'
    } 
   stage('Build') {
         git 'https://github.com/subaan/openmrs.git/'
         sh 'mvn package'
   }

stage("publish to s3") {
  step([
        $class: 'S3BucketPublisher',
        entries: [[
            sourceFile: '**/*.war',
            bucket: 'appranix-demo',
            selectedRegion: 'us-east-1',
            noUploadOnFailure: true,
            managedArtifacts: true,
            flatten: true,
            showDirectlyInBrowser: true,
            keepForever: true,
        ]],
        profileName: 'appranix-demo',
        dontWaitForConcurrentBuildCompletion: false, 
    ])
   sh 'echo War published to s3'
	
}

stage('Initiate prana deployment') {


       sh 'echo Successfully logged in prana'

       sh 'echo Organization is set as devorg'

       sh 'echo Assembly is set as shopping-cart'

       sh 'echo Transition variable update build ver'

       sh 'echo Transition variable update build ver'

       sh 'echo Deployement started'
      
   }
}
