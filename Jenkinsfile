pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master', url: 'https://github.com/Hamadkhattak/bookStoreApp.git'
            }
        }

        stage('Deploy Part 2') {
            steps {
                sh '''
                    cd /var/lib/jenkins/part2-deployment
                     docker compose -f docker-compose.part2.yml down
                     docker compose -f docker-compose.part2.yml up -d
                '''
            }
        }
    }
}
