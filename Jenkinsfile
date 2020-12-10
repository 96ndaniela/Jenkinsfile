pipeline {
   agent any
    
   environment {
      VALUE_ONE = '1'
   }
    
   stages {
       
      stage("first") {
	      steps {
            echo 'one.'
         }
      }
       
      stage('second') {
         when {
            expression {
               VALUE_ONE == '1' 
            }
         }
         steps {
            echo 'updating two.'
         }
      }
  
      stage("third") {
         when {
		 expression {
               VALUE_ONE == '2' 
            }
         }
	      steps {
		      sleep (1)}

      }
   }
}
