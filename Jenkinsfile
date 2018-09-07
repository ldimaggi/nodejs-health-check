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

      app = processTemplate(params: [
        release_version: "1.0.${env.BUILD_NUMBER}"
      ])

      echo "----------------------------------------------------"
      app = processTemplate(path: ".openshiftio/applcation.yaml", params: [
        release_version: "1.0.${env.BUILD_NUMBER}"
      ])
      echo "----------------------------------------------------"

      app = processTemplate(path: ".openshiftiofoobar/applcation.yaml", params: [
        release_version = "1.0.${env.BUILD_NUMBER}"
      ])
      echo "----------------------------------------------------"

      build app: app
    }
}
