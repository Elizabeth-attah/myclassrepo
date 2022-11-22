pipeline{
        agent any;
        stages{
                stage('SCM Checkout'){
                        step{
                                git branch: 'main', credentialsId: 'eli-cred', url: 'https://github.com/Elizabeth-attah/myclassrepo.git'
                        }

                }
                stage('Build Docker Image'){
                        steps{
                                sh 'docker build -t elizabethattah/mydockerclassrepo-1:latest .'
                        }
                }
                stage('Push Docker Image'){
                        steps{
                            sh 'docker login -u elizabethattah -p 23January'
                            sh 'docker push elizabethattah/mydockerclassrepo-1:latest'
                        }

                }
        }
}
