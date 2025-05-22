# Easy_Jenkins
### Steps to Complete:</br>
</br>
1. **Access Jenkins and Explore the Dashboard**</br>
    - Log in to your Jenkins instance</br>
    - Identify the main dashboard components (jobs list, build queue, build executor status)</br>
    - Navigate between different views if available</br>
2. **Create a Simple Pipeline Job**</br>
    - Click "New Item" on the dashboard</br>
    - Name your job "HelloJenkins"</br>
<img src ="https://github.com/user-attachments/assets/39a721c8-37a2-4abd-9f46-473e30e8cdc7"></br>
    - Select "Pipeline" as the job type</br>
    - In the pipeline script area, add this basic script:</br>
<img src ="https://github.com/user-attachments/assets/e861470f-aea9-4825-a004-262f0cbcc4da">

<pre>
groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'sleep 5'// Simulate build time
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'sleep 3'// Simulate test time
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'sleep 2'// Simulate deployment
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline execution failed!'
        }
    }
}
</pre>
​


