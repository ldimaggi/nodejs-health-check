#!/usr/bin/groovy
@Library('github.com/sthaha/fabric8-pipeline-library@build-commands')_

osio {
    config runtime: 'node'

    ci {
        def app = processTemplate()
        build app: app
    }

    cd {
      def app = processTemplate(params: [
        release_version: "1.0.${env.BUILD_NUMBER}"
      ])
      build app: app

      // test passing in commands
      build app: app, commands: """
        npm version
        ls .openshiftio
        pwd
        oc version
      """
      deploy app: app, env: 'stage'
    }
}
