#!/usr/bin/groovy
@Library('github.com/sthaha/fabric8-pipeline-library@config-api')_

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
      deploy app: app, env: 'stage'
    }
}
