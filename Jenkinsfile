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
            not {
               anyOf {
                  branch "development"
                  environment name:'VALUE_ONE', value: '4'
               }
            }
         }
	      steps {
		      sleep (1)}

      }
   }
}
