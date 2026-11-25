pipeline {
agent any
tools {
jdk 'JDK21'
maven 'Maven3'
}
stages {
stage('checkout') {
steps {git branch:'main',url:'https://github.com/Selva692/spingweb-demo1.git'}
}
stage('Build'){
steps{
sh 'mvn test'
}
}
}
post{
success{
echo 'Springweb build successfully!'
}
failure{
echo 'Build Failed'
}
}
}