#!/usr/bin/groovy
@Library('github.com/hrishin/fabric8-pipeline-library@nodejs')_


nodeJs {

    templateConfig = ["RELEASE_VERSION" : "1.0.${env.BUILD_NUMBER}"]

    cd {
        template = processTemplate templateConfig

        build template

        deploy 'stage', template

        deploy 'run', template,  true
    }
}
