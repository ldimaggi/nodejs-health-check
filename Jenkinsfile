#!/usr/bin/groovy
@Library('github.com/hrishin/fabric8-pipeline-library@nodejs')_

nodeJs {


    cd {
        appConfig = ["RELEASE_VERSION" : "1.0.${env.BUILD_NUMBER}"]

        app = processTemplate appConfig

        build app

        deploy app, 'stage'

        deploy app, 'run', approval: "manual"
    }
}
