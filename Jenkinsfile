pipeline {
    
    agent any
    
    stages {
        
        stage ("First") {
            
            tools { maven "maven3.3.9" }
            steps {
                sh "echo mvn -v"
                sh "echo First"
            }
        }
        stage ("Second") {
            
            tools { maven "maven3.3.3" }
            steps {
                sh "echo mvn -v"
                sh "echo Second"
            }
        }
        stage ("Third") {
            steps {
                sh "echo Third"
            }
        }
    }
}
