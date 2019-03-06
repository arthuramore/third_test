node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t amore_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'arthuramore' -p 'Kodisha_19' "
sh "docker tag amore_test:latest arthuramore/amore_test:latest"
sh "docker push arthuramore/amore_test:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
