node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t dockerrevision:1.0 ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'nashipae' -p 'nashnashd81#' "
sh "docker tag dockerrevision:1.0 nashipae/revision:latest"
sh "docker push nashipae/revision:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
