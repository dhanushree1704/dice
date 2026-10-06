pipeline {
    agent any

    stages {
        stage('cloning') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/YOUR_USERNAME/dicee-game.git'
            }
        }

        stage('package') {
            steps {
                bat 'mvn package -DskipTests'
            }
        }

        stage('app') {
            steps {
                bat 'mvn spring-boot:run'
            }
        }
    }
}
