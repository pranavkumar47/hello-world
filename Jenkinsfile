node {
        stage ('Clone') {
               git branch: 'master', url: "https://github.com/pranavkumar47/hello-world.git"
        }
        def mvnHome = tool 'M3'
        sh "${mvnHome}/bin/mvn -B clean package"
       
                                      
 }
  
            
                     
