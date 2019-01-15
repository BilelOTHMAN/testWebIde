@Library('piper-lib-os') _

node() {

  stage('prepare') {

      checkout scm

      checkChangeInDevelopment script: this
  }

  stage('solmanUpload') {
      transportRequestUploadFile script:this
  }
}