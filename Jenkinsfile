pipeline{
    agent none
    stages{
        stage('Build'){
            steps{
                node{sh 'git clone https://github.com/ouisaaa/jenkins_study.git'
                sh 'cd jenkins_study.git && ./gradlew build -p /spring.jar'}
            }
        }
        stage('Test'){
            steps{node{sh './gradlew test'}}
        }
        stage('Deploy'){
            steps{node{sh 'nohup java -jar /spring.jar '}}
        }
    }
}
