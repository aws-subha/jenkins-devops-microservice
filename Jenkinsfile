// Scripted 
//node {
//    echo 'Build'
//    echo 'Test'
//    echo 'Integration Test'
//}

// Declarative
pipeline {
    //agent any
    agent { docker {image 'maven:3.9.0'} }
    stages {
        stage('Build'){
            steps{
                sh 'mvn --version'
                echo"Build"
            }
        }
         stage('Test'){
            steps{
                echo"Test"
            }
        }
                stage('Integration Test'){
            steps{
                echo"Integration Test"
            }
        }
    }
    post{
        always{
            echo 'Im awesome . I run always'
        }
        success{
            echo 'I run when build successful'
        }
        failure{
            echo 'I run when build Fail'
        }
    }
}
