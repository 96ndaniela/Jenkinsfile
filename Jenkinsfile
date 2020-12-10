pipeline {
    agent any
	stages {
		stage('first') {
			steps {
				{
					env.execute="True"
				echo "first"
				}
			}


		stage('second') {
			steps {
				when { 
				$env.execute="True"
				echo "updating second stage."}
				}
			} 

		stage('third') {
			steps {
				when $env.execute="False"
				echo "third"
				}
			}
		}
} 
 
