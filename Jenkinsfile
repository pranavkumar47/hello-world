pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                git branch: 'master', url: "https://github.com/jfrog/project-examples.git"
            }
        }

        stage ('Artifactory configuration') {
          
                rtMavenDeployer (
                    id: "MAVEN_DEPLOYER",
                    releaseRepo: "libs-release-local",
                    snapshotRepo: "libs-snapshot-local"
                )

              }
        }

        stage ('Exec Maven') {
            steps {
                rtMavenRun (
                    tool: MAVEN_TOOL, // Tool name from Jenkins configuration
                    pom: 'hello-world/pom.xml',
                    goals: 'clean install',
                    deployerId: "MAVEN_DEPLOYER",
  
                )
            }
        }

                
            }
        }
    }
}
