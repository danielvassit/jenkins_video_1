pipeline {
    
    agent any 
    
    environment {
        FOO="BAR"
    }
    
    stages {
        stage ("First") {
            tools { maven "maven3.3.9" }
            steps {
                sh "mvn -v"
                sh "echo first"
            }
            post {
                always {
                    sh "echo $FOO"   
                }
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
                parallel (
                    one: {
                        echo "1"
                    },
                    two: {
                        echo "2"
                    },
                    three: {
                        echo "3"
                    }
                )
            }
        }
    }
}