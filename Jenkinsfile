@Library('piper-lib-os') _

node() {

  stage('prepare') {

      checkout scm

      checkChangeInDevelopment script: this
								       changeManagement: [
							                               credentialsId: '12dd7492-a47d-4723-955d-83340217241f'
							                               endpoint: 'ns3026258.ovee.fr'
							                               type: 'SOLMAN'
							                             ]
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
  }
}