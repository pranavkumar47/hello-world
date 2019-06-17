node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   git branch: 'master', url: "https://github.com/jfrog/project-examples.git"
      stage ('Exec Maven') {
           mvn 'clean' 'install'
}
}
