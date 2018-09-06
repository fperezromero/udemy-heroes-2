pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Stage 1') {
      steps {
        bat(script: 'echo "estoy ejecutando la primera etapa', returnStatus: true, returnStdout: true)
        bat(script: 'dir C:\\Users\\Marie Macharackova\\Documents\\curso_gif ', returnStatus: true, returnStdout: true)
      }
    }
    stage('Stage 2') {
      steps {
        echo 'Estamos en Stage 2'
        git 'https://github.com/fperezromero/udemy-heroes-2.git'
      }
    }
    stage('Stage 3') {
      steps {
        readFile '*.*'
        powershell(script: 'Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE -ComputerName . | Format-Table -Property IPAddress', returnStdout: true, returnStatus: true)
      }
    }
  }
}