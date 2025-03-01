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
            node{steps{sh './gradlew test'}}
        }
        stage('Deploy'){
            node{steps{sh 'nohup java -jar /spring.jar '}}
        }
    }
}
