pipeline {
    
    agent any 
    
    
    stages {
        stage ("First") {
            tools { maven "maven3.3.9" }
            steps {
                sh "mvn -v"
                sh "echo first"
            }
        }
        
        stage ("Second") {
            tools { maven "maven3.3.9" }
            steps {
                sh "mvn -v"
                sh "echo second"
            }
        }
        
        stage ("Third") {
            steps {
                sh "echo third"
            }
        }
    }
}