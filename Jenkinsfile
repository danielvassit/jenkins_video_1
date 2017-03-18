pipeline {
    
    agent any
    
    stages {
        
        stage ("First") {
            steps {
                tools { mvn "maven3.3.9" }
                sh "echo First"
            }
        }
        stage ("Second") {
            steps {
                tools { mvn "maven3.3.3" }
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
