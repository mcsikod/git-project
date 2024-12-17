pipeline {
    agent any

    stages {
        stage('cloning') {
            steps {
                echo 'cloning thee git repository..'
            }
        }
stage('test') {
            steps {
                echo 'testing source code..'
                  sh ‘sonnar sonnar’
            }
        }
stage('Buildjar') {
            steps {
                echo 'Building the jar artifact..'
                  sh ‘mvn package’
            }
        }
stage('deploy to nexus') {
            steps {
                echo 'deploying build artifact to nexus..'
                 sh ‘mvn deploy’
            }
        }
stage('Build image') {
            steps {
                echo 'building image from Dockerfile..'
                  sh ‘docker build -t myapp:1.0 ,’
            }
        }
stage('deploy APP') {
            steps {
                echo 'deploying build artifact to nexus..'
                  sh ’kubectl apply -f manifest file’
            }
        }
stage('verify app') {
            steps {
                echo 'application successfully deploy’
            }
        }
