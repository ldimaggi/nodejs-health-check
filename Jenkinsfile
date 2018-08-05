#!/usr/bin/groovy
@Library('github.com/hrishin/osio-pipeline@cd-fixes')

def STAGES = ['run', 'stage']

openshift.withCluster() { //r fallback to OpenShift cluster detection
    echo "Hello from the project running Jenkins: ${openshift.project()}"
}

osio {
  stages = STAGES
}
