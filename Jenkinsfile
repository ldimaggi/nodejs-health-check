#!/usr/bin/groovy
@Library('github.com/hrishin/osio-pipeline@template-param-fix')

def STAGES = ['run', 'stage']
def templateParameters = ["SUFFIX_NAME": "", "RELEASE_VERSION": "1.0.${env.BUILD_NUMBER}"]

osio {
  templateConfig = templateParameters
  stages = STAGES
}
