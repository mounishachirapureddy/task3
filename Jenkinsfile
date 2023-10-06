pipeline {
    agent any

    tools {
        // Use the Git Tool configuration 'Default' or specify the correct one.
        git 'Default'
    }

    stages {
        stage('Checkout') {
            // Checkout code from the 'main' branch
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: 'main']],
                    userRemoteConfigs: [[
                        url: 'https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/Snapcoins',
                        credentialsId: 'AWS' // Use the correct credentials ID
                    ]],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: []
                ])
            }
        }
    }
}
