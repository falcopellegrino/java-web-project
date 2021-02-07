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
                deploy adapters: [tomcat7(credentialsId: 'd5b70da9-deab-4966-a3c2-ea8e8b2d61bc', path: '', url: 'http://18.220.2.156:8080/')], contextPath: 'javawebapp', war: 'http://3.139.66.214:8080/'
            }
        }
    }
}
