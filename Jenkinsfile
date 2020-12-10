pipeline {
    agent any
	environment{
	one='1'}
		stages {
			stage('first') { 
			when {one == '1'}
				steps {
					sh echo "step one"
					}
			}


			stage('second') {
			when {one == '1'}
				steps {
					sh echo "updating step two"
					sh echo "step two"
					}
			} 

			stage('third') {
                	when {one == '2'}
				steps {
					when $envone="False"
					sh echo "step three"
					}
			}
		}
}
