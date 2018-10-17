#!groovy

import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import jenkins.util.*;
import jenkins.model.*;
import java.net.URL

node('site'){
ws('/var/www/html'){ 
   stage('Preparation') { 
      checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'WipeWorkspace'], [$class: 'CleanBeforeCheckout']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GIT', url: 'https://github.com/naveenkashyapdv/my-site.git']]]
     }
     stage('Preparation')
         sh 'service nginx restart'
    }
}
