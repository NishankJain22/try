pipeline {
	agent any
	stages {
		stage ("Clone") {
			steps {
				script {
					git 'https://github.com/NishankJain22/try.git';
						}
				}
			}
			
		stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                    bat(/${MAVEN_HOME}\bin\mvn -Dmaven.test.failure.ignore clean deploy sonar:sonar/)
                }
            }
        }
		}
	}