// pipeline {
//     agent any
    
//     stages {
//         stage('Hello') {
//             steps {
//                 echo 'Hello, World!'
//             }
//         }
//     }
// }

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
              checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'aeb0c383-d05e-4adf-9cab-e2a2f3f3d2e9', url: 'https://github.com/Mitalib2001/task2arxml.git']])
            }
        }
        stage('Run Script') {
            steps {
               sh 'python3 script.py -i AutosarFile.xml -o output1.xlsx  '
            }
        }
    }
}
