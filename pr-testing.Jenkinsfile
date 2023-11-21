pipeline {
    agent any

    stages {
        stage('Unittest') {
            steps {
                script {
                    sh """
                        pip install pytest
                        python3 -m pytest --junitxml results.xml tests
                    """
                }
            }
        }
        stage('Lint') {
            steps {
                echo "linting_____"
            }
        }
        stage('Functional test') {
            steps {
                echo "testing__"
            }
        }
    }
}
