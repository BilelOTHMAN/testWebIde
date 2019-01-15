@Library('piper-lib-os') _

node() {

  stage('prepare') {

      checkout scm

      checkChangeInDevelopment script: this
								       changeManagement: [
							                               endpoint: 'ns3026258.ovee.fr'
							                             ]
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
  }
}