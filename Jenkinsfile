pipeline {
  agent {
    label 'golang'
  }
  stages {
    stage('Checkout') {
      steps {
        echo "Checkout"
      }
    }
    stage('CI') {
      parallel {
        stage('Test1') {
          steps {
            echo "CI Test3..."  
          }
        }
        stage('Test4') {
          steps {
            echo "CI Test4..."  
            echo "CI Test4..."  
          }
        }
        stage('Test6') {
          steps {
            echo "CI Test6..." 
          }
        }
      }
    }
    stage('CI1') {
      parallel {
        stage('Build1') {
          steps {
            echo "CI Build...CI Build...CI Build...CI Build...CI Build...CI Build...CI Build..." 
          }
        }
        stage('Test1') {
          steps {
            echo "CI Test1...CI Test1...CI Test1...CI Test1...CI Test1...CI Test1..."  
          }
        }
      }
    }
    stage('scan') {
      steps {
        echo alaudaContext.isSupport()? "true":"false"
        echo alaudaContext.getNamespace()
      }
    }
    stage('Deploy2') {
      steps {
        echo "Deploy2..."
      }
    }
  }
}
