pipeline {
    agent any
    tools { 
        maven 'mavenv3' 
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/RayyanSameer/SpringPetClinic.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

       // stage('Deploy') {
        //    steps {
            //    sh 'java -jar target/*.jar'
           // }
       // }
    }
}
