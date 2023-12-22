pipeline {
    agent any
    environment {
       dotnet = '"C:\\Program Files\\dotnet\\dotnet.exe"'
    }


    stages {
       
          stage('Build') {
                steps {
                   dir("unit-testing-using-nunit"){
                    bat "${dotnet} build"
                   }
                }
            }

            stage('Testing') {
                steps {
                   dir("unit-testing-using-nunit"){
                    bat "${dotnet} test"
                   }
                }
            }

            stage('Cleanimng') {
                steps {
                   dir("unit-testing-using-nunit"){
                    bat "${dotnet} clean"
                   }
                }
            }

    }
}
