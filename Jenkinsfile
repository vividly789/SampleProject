def workspace;
node
{
    stage('Checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0e58c990-80af-43ea-9f55-85c176bba12b', url: 'https://github.com/samsonawane/SampleProject.git']]])
        workspace =pwd()
    }
    stage('Static Code Analysis')
    {
        def sonarHome = tool 'Sonar-Scanner';
        withSonarQubeEnv('SonarQubeServer') {
            sh """${scannerHome}/bin/sonar-runner -D sonar.login=admin -D sonar.password=admin"""
        }
    }
    stage('Build')
    {
        echo "Build the code"
    }
    stage('Unit Testing')
    {
        echo "Unit Testing"
    }
    stage ('Delivery')
    {
        echo "Devliver the Code"
    }
    
}
