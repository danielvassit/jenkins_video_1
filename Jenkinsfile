pipeline {
    
    environment {
        FOO="BAR"
    }
    
    agent any
    
    stages {
        
        stage ("First") {
            
            tools { maven "maven3.3.9" }
            steps {
                sh "mvn -v"
                sh "echo First"
            }
            
            post {
                always {
                    sh "echo $FOO" 
                }
            }
        }
        stage ("Second") {
            
            tools { maven "maven3.3.3" }
            steps {
                sh "mvn -v"
                sh "echo Second"
            }
        }
        stage ("Third") {
            steps {
                parallel (
                    one: {
                        sh "echo 1"
                    }
                    two: {
                        sh "echo 2"
                    }
                    three: {
                        sh "echo 3"
                    }
                )
                }
            }
        }
    }
}
