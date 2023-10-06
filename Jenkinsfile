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
                        credentialsId: '65b859fa-8c76-49a5-b70c-53b42326b02c' // Use the correct credentials ID
                    ]],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: []
                ])
            }
        }
    }
}
