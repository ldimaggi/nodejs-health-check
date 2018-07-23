#!/usr/bin/groovy

@Library('github.com/hrishin/osio-pipeline@master')
def STAGES = ['run', 'stage']

openshift.withCluster() { // Use "default" cluster or fallback to OpenShift cluster detection
    echo "Hello from the project running Jenkins: ${openshift.project()}"
}

osio {
  stages = STAGES
}
