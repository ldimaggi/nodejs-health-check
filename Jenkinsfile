#!/usr/bin/groovy

@Library('github.com/fabric8io/osio-pipeline@master')

def STAGES = ['run', 'stage']

sh "env"
openshift.withCluster() { //r fallback to OpenShift cluster detection
    echo "Hello from the project running Jenkins: ${openshift.project()}"
}

osio {
  stages = STAGES
}
