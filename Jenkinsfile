pipeline
{
    agent any
    environment {
        AUTHOR = "pragra"
        class = "devops"
        batch = "Jan23"
    }
    stages {
        stage('BUILD')
        {
            steps
            {
                sh 'mvn clean install -DskipTests'
            } 
        }
        stage('UNIT TESTS')
        {
            steps
            {
                sh 'printenv'
                sh 'mvn test'
            }
        }

        stage('INTEGRATION TESTS')
        {
            steps
            {
                sh ''
                sh 'mvn verify -DskipUnitTests'
            }
        }

        stage('CODE ANALYSIS') 
        {
            steps
            {
                sh 'mvn checkstyle:checkstyle'
            }
        }
    }
}
