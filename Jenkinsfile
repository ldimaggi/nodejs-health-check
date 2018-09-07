#!/usr/bin/groovy
@Library('github.com/sthaha/fabric8-pipeline-library@nodejs')_

osio {
    ci {
        app = processTemplate()
        build app: app
    }

    cd {
      app = processTemplate() {
        // override the default release version parameter
        release_version = "1.0.${env.BUILD_NUMBER}"
      }
      build app: app
      deploy app: app, env: 'stage'
    }
}
