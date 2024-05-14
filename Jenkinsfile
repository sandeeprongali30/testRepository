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
//         echo "Testing the Application1..."
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
        nodejs('nodejs-20.2'){
            sh 'yarn install'
        }
      }
    }
    stage("Node"){
      steps{
        echo "executing Gradle..."
        withGradle(){
            sh 'Gradle -version'
        }
      }
    }
  }
}
