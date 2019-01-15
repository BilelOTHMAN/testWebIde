@Library('piper-lib-os') _

node() {
  def mtarFileName
  stage('prepare') {

      checkout scm
	  setupCommonPipelineEnvironment script: this, configFile: 'pipeline/config.yml'
	  prepareDefaultValues script: this
	  mtarFileName = mtaBuild script:this, buildTarget: 'NEO'
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
    							filePath : mtarFileName
  }
}