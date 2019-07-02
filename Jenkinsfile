node('with-basic-tools'){
    stage("Check Out") {
        git changelog: false, poll: false, url: "https://github.com/bmunozm/parallel-test-executor-plugin.git", branch: "master"
    }
	sh "mvn test -Dtest=ParallelTestExecutorTest#splitTestsEstimateTestsFromFiles -Denforcer.skip"
}
node('windows-testing'){
    stage("Check Out") {
        git changelog: false, poll: false, url: "https://github.com/bmunozm/parallel-test-executor-plugin.git", branch: "master"
    }
	bat "mvn test -Dtest=ParallelTestExecutorTest#splitTestsEstimateTestsFromFiles -Denforcer.skip"
}