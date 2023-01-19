pipeline {
agent {label 'dev'}
triggers {
  pollSCM '* * * * *'
}
stages{
stage('scm'){
steps{
checkout scmGit(branches: [[name: '*/feat01']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prprusty/mavenrepo.git']])
}
}
stage('build'){
steps{
sh 'mvn package'
}
}

}
}
