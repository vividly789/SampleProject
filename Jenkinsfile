def workpace;
node
{
    stage('checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/vividly789/SampleProject.git']]])
        workspace =pwd()
    }
    stage('static code analysis')
    {
        echo "static code analysis"
    }
    stage('build')
    {
        echo "build the code"
    }
    stage('unit testing')
    {
        echo "unit testing"
    }
    stage('delivery')
    {
        echo "deliver the code"
    }
    
}
