pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                git branch: 'master', url: "https://github.com/JayaharRajkumar/eCommerce.git"
            }
        }

        stage ('Exec Maven') {
            steps {
                rtMavenRun (
                    tool: MAVEN_TOOL, // Tool name from Jenkins configuration
                    pom: 'pom.xml',
                    goals: 'clean install'
                )
            }
        }

    }
}