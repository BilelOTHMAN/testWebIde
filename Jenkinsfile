@Library('piper-lib-os') _

node() {

  stage('prepare') {

      checkout scm
	  setupCommonPipelineEnvironment script: this, configFile: 'pipeline/config.yml'
	  prepareDefaultValues script: this
      checkChangeInDevelopment script: this
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
  }
}