pipeline {
   agent any
    
   environment {
      VALUE_ONE = '1'
   }
    
   stages {
       
      stage("first") {
         when {
		    branch 'master'
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
            not {
               anyOf {
                  branch "development"
                  environment name:'VALUE_ONE', value: '4'
               }
            }
         }
         steps {
            exit
         }
      }
   }
}
