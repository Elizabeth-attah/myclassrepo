pipeline{
        agent any;
        stages{
                stage('SCM Checkout'){
                        steps{
                                git branch: 'main', credentialsId: https://github.com/Elizabeth-attah/myclassrepo.git'
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
                            sh 'docker push elizabethattah/mydockerclassrepo-1:latest .'
                        }

                }
        }
}
