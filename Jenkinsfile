#!/usr/bin/groovy
@Library('github.com/sthaha/fabric8-pipeline-library@config-api')_

osio {
    ci {
        app = processTemplate()
        build app: app
    }

    cd {
      app = processTemplate(params: [
        release_version: "1.0.${env.BUILD_NUMBER}"
      ])
      echo "----------------------------------------------------"

      build app: app
    }
}
