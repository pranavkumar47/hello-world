pipeline {
    agent any
    stages {
        stage ('Clone') {
               git branch: 'master', url: "https://github.com/pranavkumar47/hello-world.git"
        }
        stage ('Exec Maven') {
                   sh 'mvn -B clean package'
        }                              
    }
}
  
            
                     
