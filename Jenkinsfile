pipeline{
 agent any
 tools{
  gradle 'Gradle'
  jdk 'jdk'
 }
 stages{
  stage('Checkout'){
   steps{
    git branch:'master',url:'https://github.com/Prajna1101/GradleDemo.git'
   }
  }
  stage('Build'){
   steps{
    sh 'gradle build'
   }
  }
  stage('Test'){
   steps{
    sh 'gradle test'
   }
  }
  stage('Run Application'){
   steps{
    sh 'gradle run'
   }
  }
 }
 post{
  success{
   echo 'Build and deploy successful!'
  }
  failure{
   echo 'Build failed!'
  }
 }
}
