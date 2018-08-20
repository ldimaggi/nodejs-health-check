#!/usr/bin/groovy
@Library('github.com/hrishin/fabric8-pipeline-library@nodejs')_

osio {

    cd {
        //appConfig = ["RELEASE_VERSION" : "1.0.${env.BUILD_NUMBER}"]

        app = processTemplate(release_version: "1.0.${env.BUILD_NUMBER}")

        build app: app

        deploy app: app, env: 'stage'

        deploy app: app, env: 'run', approval: "manual"
    }
}
