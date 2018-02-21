pipeline {
  agent any
  stages {
    stage('Master_A') {
      steps {
        parallel(
          "Master_A": {
            node(label: 'Master') {
              bat(script: 'Wscript "C:\\Devaraj\\Test\\a.vbs"', returnStatus: true, returnStdout: true)
            }
            
            
          },
          "Slave_B": {
            node(label: 'Sid_Machine') {
              bat(script: 'Wscript "C:\\Devaraj\\Test.b.vbs"', returnStatus: true, returnStdout: true)
            }
            
            bat(script: 'Wscript "C:\\Devaraj\\Test\\b.vbs"', returnStatus: true, returnStdout: true)
            
          }
        )
      }
    }
  }
}