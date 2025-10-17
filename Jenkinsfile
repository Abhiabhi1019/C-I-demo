pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Abhiabhi1019/C-I-demo.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }
        stage('Debug') {
            steps {
                sh 'ls -la'
                sh 'pwd'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'python3 -m unittest discover -s . -p "test_*.py"'
            }
        }
    }
}

