rrpBuildGoCode {
    projectKey = 'expect'
    testDependencies = ['mongo']
    dockerBuildOptions = ['--squash', '--build-arg GIT_COMMIT=$GIT_COMMIT']
    ecrRegistry = "280211473891.dkr.ecr.us-west-2.amazonaws.com"
    dockerImageName = "rsp/${projectKey}"
    protexProjectName = 'bb-expect'
    buildImage = 'amr-registry.caas.intel.com/rrp/ci-go-build-image:1.12.0-alpine'

    infra = [
        stackName: 'RSP-Codepipeline-Expect'
    ]

    notify = [
        slack: [ success: '#ima-build-success', failure: '#ima-build-failed' ]
    ]
}
