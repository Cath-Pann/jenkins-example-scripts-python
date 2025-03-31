// pipeline {
//   agent {

//   }
//   stages {
//     stage('version') {
//       steps {
//         sh 'python3 --version'
//       }
//     }
//     stage('hello') {
//       steps {
//         sh 'python3 hello.py'
//       }
//     }
//   }
// }

pipeline {
    agent any
    stages{
      stage('build'){
        agent {
          docker {
            image 'python:3.9'
          }
        }
        steps {
                sh'''
                    python --version

                '''
            }
      }
      stage ('hello'){
        agent {
          docker {
            image 'python:3.9'
          }
        }
        steps {
          sh 'python3 hello.py'
        }
      }
    
    }
             
}