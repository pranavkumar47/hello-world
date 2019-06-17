node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   git branch: 'master', url: "https://github.com/jfrog/project-examples.git"
      stage ('Exec Maven') {
            steps {
                rtMavenRun (
                    tool: MAVEN_TOOL, // Tool name from Jenkins configuration
                    pom: 'maven-example/pom.xml',
                    goals: 'clean install',
                    deployerId: "MAVEN_DEPLOYER",
                    resolverId: "MAVEN_RESOLVER"
                )
            }
}
}
