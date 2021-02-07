pipeline{
    agent any
    options {
      timeout(30)
    }
    stages{
        
             stage('Mvn Build'){
                steps{
                    bat 'mvn clean package'
                }
            }
        
     
        }
}
