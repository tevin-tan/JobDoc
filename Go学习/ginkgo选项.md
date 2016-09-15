# Usage of ginkgo: #

	  -afterSuiteHook="": Run a command when a suite test run completes
	
	  -compilers=0: The number of concurrent compilations to run (0 will autodetect)
	
	  -cover=false: Run tests with coverage analysis, will generate coverage profiles with the package name in the current directory
	
	  -coverpkg="": Run tests with coverage on the given external modules
	
	  -dryRun=false: If set, ginkgo will walk the test hierarchy without actually running anything.  Best paired with -v.
	
	  -failFast=false: If set, ginkgo will stop running a test suite after a failure occurs.
	
	  -failOnPending=false: If set, ginkgo will mark the test suite as failed if any specs are pending.

	  -flakeAttempts=1: Make up to this many attempts to run each spec. Please note that if any of the 
	   attempts succeed, the suite will not be failed. But any failures will still be recorded.
	 
	  -focus="": If set, ginkgo will only run specs that match this regular expression.

	  -gcflags="": Arguments to pass on each go tool compile invocation.

	  -keepGoing=false: When true, failures from earlier test suites do not prevent later test suites from running

	  -noColor=false: If set, suppress color output in default reporter.

	  -nodes=1: The number of parallel test nodes to run

	  -noisyPendings=true: If set, default reporter will shout about pending tests.

	  -p=false: Run in parallel with auto-detected number of nodes

	  -progress=false: If set, ginkgo will emit progress information as each spec runs to the GinkgoWriter.

	  -r=false: Find and run test suites under the current directory recursively

	  -race=false: Run tests with race detection enabled

	  -randomizeAllSpecs=false: If set, ginkgo will randomize all specs together.  By default, ginkgo only randomizes the top level Describe/Context groups.

	  -randomizeSuites=false: When true, Ginkgo will randomize the order in which test suites run

	  -regexScansFilePath=false: If set, ginkgo regex matching also will look at the file path (code location).

	  -seed=1473957070: The seed used to randomize the spec suite.

	  -skip="": If set, ginkgo will only run specs that do not match this regular expression.

	  -skipMeasurements=false: If set, ginkgo will skip any measurement specs.

	  -skipPackage="": A comma-separated list of package names to be skipped.  If any part of the package's path matches, that package is ignored.

	  -slowSpecThreshold=5: (in seconds) Specs that take longer to run than this threshold are flagged as slow by the default reporter.

	  -stream=true: stream parallel test output in real time: less coherent, but useful for debugging

	  -succinct=false: If set, default reporter prints out a very succinct report

	  -tags="": A list of build tags to consider satisfied during the build

	  -trace=false: If set, default reporter prints out the full stack trace when a failure occurs

	  -untilItFails=false: When true, Ginkgo will keep rerunning tests until a failure occurs

	  -v=false: If set, default reporter print out all specs as they begin.
