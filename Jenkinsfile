pipeline{
  agent any
  tools{
    gardle 'Gradle'
    jdk 'JDK'
    }
  stages{
    stage('checkout'){
      steps{
        git branch:"master",url:"https://github.com/srushtiiik/exmgrad.git"
        }
      }
    stage('build'){
      steps{
        sh 'gradle build'
        }
       }
    stage('deploy'){
      steps{
        sh 'gradle test'
        }
       }
    stage('run'){
      steps{
        sh 'gradle run'
        }
       }
post{
  success{
    echo "succuss"
    }
  failure{
    echo "failure"
   }
  }
 }
