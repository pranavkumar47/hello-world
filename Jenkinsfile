node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

  git url:https://github.com/pranavkumar47/hello-world.git
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
