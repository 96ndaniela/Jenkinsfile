pipeline {
   agent any
    
   environment {
      VALUE_ONE = '1'
   }
    
   stages {
       
      stage("first") {
         when {
		   expression {
               VALUE_ONE == '1' 
            }
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
            not {VALUE_ONE == '4'
               }
            }
         }
         steps {
         }
      }
   }
}
 
