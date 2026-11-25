pipeline {
agent any
stages {
stage('checkout') {
steps {'Checking Github Project'}
}
stage('Build'){
steps{
sh 'chmod +x mvnw'
sh './mvnw clean package-DskipTests'
}
}
stage('Test'){
steps{
sh './mvnw test'
}
}
stage('Docker Build'){
steps{
sh 'docker bulid -t springweb-demo1:latest .'
}
}
}
post{
success{
echo 'Springweb and Docker build Successful!'
}
failure{
echo 'Pipeline Failed.Check Console Output'
}
}
}