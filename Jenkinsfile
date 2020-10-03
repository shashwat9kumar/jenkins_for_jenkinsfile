pipeline{
    agent any
    stages{
      stage('Start'){
          steps{
          echo 'Start the Pipeline'
          }
      }
        
        
        stage('Clean phase Starts'){
          steps{
          echo 'Start the Clean phase'
          }
      }
      stage('Clean'){
          steps{
          bat 'mvn clean'
          }
      }
        
        
        stage('Install phase Starts'){
          steps{
          echo 'Start the Instll phase'
          }
      }
        stage('Install'){
          steps{
          bat 'mvn install'
          }
      }
        
       
        stage('Test phase Starts'){
          steps{
          echo 'Start the Test phase'
          }
      }
        stage('Test'){
          steps{
          bat 'mvn test'
          }
      }
        
       
        
      stage('Sonar phase Starts'){
          steps{
          echo 'Start the Sonar phase'
          }
      }  
      stage('Sonar'){
          steps{
            bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.analysis.mode=publish'
          }
      }
    }
}
