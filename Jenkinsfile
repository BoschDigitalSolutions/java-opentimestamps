@Library('bds-pipeline') _

pipeline {

   agent any

   options { 
      buildDiscarder(logRotator(numToKeepStr: '10')) 
   }

   stages {
       stage('Maven Build') {
           steps {
               mavenBuild name: "java-opentimestamps", javaVersion: "java-11"
           }
       }
   }
}