pipeline{
    agent any{
        stage('Build'){
            steps{
                sh '-B -DskipTests clean package'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}