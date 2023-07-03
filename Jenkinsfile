pipeline {
	agent any 
	stages{
		stage('1-clonecode'){
			steps{
			sh 'echo "welcome to jenkins demo"'
			}
		}
		stage('2-s2'){
			steps{
				sh 'lscpu'
				sh 'whoami'
			}
		}
		stage('3-s3'){
			steps{
				sh 'df -h'
				sh 'touch team6'
			}
		}
		stage('4-s4'){
			steps{
				sh 'pwd'
				sh 'du -h'
			}
		}
        stage('5-s5'){
			parallel {
				stage('p1'){
					steps{
						echo "first parallel-stage"
					}
				}
				stage('p2'){
					steps{
						echo "second parallel-stage"
					}
				}
			}
        }
        stage('6-scriptdemo'){
            steps{
                sh 'echo "this is the end"'
            }
        }
	}
}