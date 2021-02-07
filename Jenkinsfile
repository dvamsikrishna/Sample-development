pipeline{
    agent any
    options {
      timeout(30)
    }
    stages{
        
             stage('Mvn Build'){
                steps{
                    sh 'mvn clean package'
                }
            }
        
     
        }
}
