// pipeline{
//   agent any
//   stages{
//     stage("Build"){
//       steps{
//         echo "Building the Application test..."
//       }
//     }
//     stage("Test"){
//       steps{
//         echo "Testing the Application..."
//       }
//     }
//   }
// }
pipeline{
  agent any
  stages{
    stage("Run FrontEnd"){
      steps{
        echo "Executing Yarn..."
        nodejs('NodeJs')
            sh 'yarn install'
        }
      }
    }
    stage("Node"){
      steps{
        echo "executing gradle..."
        with Gradle(){
            sh './gradlew -v'
        }
      }
    }
  }
}
