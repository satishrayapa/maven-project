pipeline {
    agent any
    options { timeout (time: 1, unit: 'HOURS') }
    stages {
        stage ('print text') {
            steps {
                echo "hello world"
            }
            input { message "should we continue"  }
        }    
        stage ('check out') {
            steps {
                git 'https://github.com/jleetutorial/maven-project.git'
            }
        }
        stage ('print statements') {
            parallel {
                stage ('print name') {
                    steps {
                        echo "my name is donald"
                    }
                }
                stage ('print job') {
                    steps {
                        echo "software engineer"
                    }
                }   
                stage ('check out') {
                    
                    steps {
                        git 'https://github.com/jleetutorial/maven-project.git'
                    }
                
                }
            }
        }
        
    }   
    post {
        always {
            echo "job is successful"
        }
    }
}   
    
  
