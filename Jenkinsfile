@Library('piper-lib-os') _

node() {

  stage('prepare') {

      checkout scm

      setupCommonPipelineEnvironment script:this

      checkChangeInDevelopment script: this
  }

  stage('build') {
      mtaBuild script: this
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
  }
}