#!/usr/bin/groovy
@Library('github.com/sthaha/fabric8-pipeline-library@nodejs')_

osio {
    ci {
        app = processTemplate()
        build app: app
    }

    cd {
      app = processTemplate()

      echo "----------------------------------------------------"
      v =  "1.0.${env.BUILD_NUMBER}"
      app = processTemplate() {
        // override the default release version parameter
        release_version = v
      }
      echo "----------------------------------------------------"

      app = processTemplate() {
        // override the default release version parameter
        release_version = "1.0.${env.BUILD_NUMBER}"
      }

      echo "----------------------------------------------------"
      build app: app
    }
}
