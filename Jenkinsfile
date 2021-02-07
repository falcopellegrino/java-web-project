pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Deploy"){
            steps{
                deploy adapters: [tomcat7(credentialsId: 'd5b70da9-deab-4966-a3c2-ea8e8b2d61bc', path: '', url: 'http://18.217.39.117:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'            }
        }
    }
}
