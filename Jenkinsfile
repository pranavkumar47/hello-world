pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                git branch: 'master', url: "https://github.com/pranavkumar47/hello-world.git"
            }
        }
                  stage ('Exec Maven') {
                   
                    pom: 'hello-world/pom.xml',
                    goals: 'clean install',
                                 
                        }
    }
}
  
            
                     
