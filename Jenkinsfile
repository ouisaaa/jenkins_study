pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'git clone https://github.com/ouisaaa/jenkins_study.git'
                sh 'cd jenkins_study.git && ./gradlew build -p /spring.jar'
            }
        }
        stage('Test'){
            steps{sh './gradlew test'}
        }
        stage('Deploy'){
            steps{sh 'nohup java -jar /spring.jar '}
        }
    }
}
