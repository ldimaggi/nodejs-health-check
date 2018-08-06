#!/usr/bin/groovy
@Library('github.com/hrishin/osio-pipeline@cd-fixes')

def STAGES = ['run', 'stage']
def templateParameters = ["SUFFIX_NAME": "", "RELEASE_VERSION": "1.0.${env.BUILD_NUMBER}"]

osio {
  stages = STAGES
}
