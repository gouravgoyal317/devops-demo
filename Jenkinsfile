pipeline {
    
   agent any

   stages {
 
       stage('Git checkout') {
        
           steps {
               echo 'Code Cloning Stage'
           }
       }

       stage('Build') {
           
           steps {
               sh 'mvn clean package'
           }
       }
      
      stage('test') {
          steps {
              echo 'Testing Stage'
          }
      }
   
      stage('Deploy') {
          steps {
              echo 'Deployment Stage'
          }
      }
   }
}
