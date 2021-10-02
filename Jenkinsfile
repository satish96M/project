pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                echo 'Code Validation..'
		sh 'mvn validate'
            }
        }
        stage('UnitTest') {
            steps {
                echo 'Unit Testing..'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
                echo 'Analysis On Bugs....'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://34.228.17.79:9000: -Dsonar.login=5915b3f56acfb3ce307afeaf749017e08e223a93'
            }
        }
    }
}
