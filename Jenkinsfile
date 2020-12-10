pipeline {
    agent any
		stages {
			stage('first') {
				envone="True"
				steps {
					sh echo "step one"
				}
			}


			stage('second') {
				when $envone="True"
				steps {
					sh echo "updating step two"
					sh echo "step two"
				}
			} 

			stage('third') {
				steps {
					when $envone="False"
					sh echo "step three"
				}
			}
		}
}

