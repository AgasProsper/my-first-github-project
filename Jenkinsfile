pipeline {
    environment {
        IMAGE_NAME="agasprosper/simple-java-pipeline-project:${BUILD_ID}"
    }
    agent any
    tools {
        maven "Maven"
    }

September's discounts are nearly yours. Be ready for 70% off Shared Hosting, 62% off EasyWP, and 33% off Private Email. Prepare to pack and move for less.

        stage ("Build DockerImage") {
            steps {
                sh "docker build -t $IMAGE_NAME ."
            }
        } 
        stage ("Pushing to Docker Hub") {
            steps {
                script{
                    withCredentials([usernamePassword(credentialsId: 'jenkins-to-access-dockerhub', passwordVariable: 'PASS', usernameVariable: 'USER')]) {
                        sh "echo $PASS | docker login -u $USER --password-stdin"
                        sh "docker push $IMAGE_NAME"
                    }
                }
            }
        }

                    }
                    
                }
            }
        }
    }
}
