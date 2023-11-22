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

            post {
                always {
                    junit allowEmptyResults: true, testResults: 'results.xml'
                }
            }
        }

        stage('Lint') {
            steps {
                echo "linting___"
            }
        }

        stage('Functional test') {
            steps {
                echo "testing__"
            }
        }
    }
}
