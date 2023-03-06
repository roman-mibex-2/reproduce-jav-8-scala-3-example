# Reproduce:

Run: mvn compile

You will get this error:

    [INFO] --- scala-maven-plugin:4.7.2:compile (compile) @ java-scala-fail-compile ---
    [INFO] Using incremental compilation using Mixed compile order
    [INFO] compiling 1 Scala source and 1 Java source to /tmp/reproduce-jav-8-scala-3-example/target/classes ...
    [ERROR] : 1.8 is not a valid choice for -java-output-version
    [INFO] :   scalac -help  gives more information
    [ERROR] one error found
    [INFO] ------------------------------------------------------------------------
    [INFO] BUILD FAILURE
    [INFO] ------------------------------------------------------------------------
    [INFO] Total time: 1.689 s
    [INFO] Finished at: 2023-03-06T16:47:00+01:00
    [INFO] ------------------------------------------------------------------------
    [ERROR] Failed to execute goal net.alchim31.maven:scala-maven-plugin:4.7.2:compile (compile) on project java-scala-fail-compile: Execution compile of goal net.alchim31.maven:scala-maven-plugin:4.7.2:compile failed: Compilation failed: InterfaceCompileFailed -> [Help 1]
    [ERROR]
    [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
    [ERROR] Re-run Maven using the -X switch to enable full debug logging.
    [ERROR]
    [ERROR] For more information about the errors and possible solutions, please read the following articles:
    [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/PluginExecutionException

When changing the version of scala-maven-plugin in pom.xml back to 4.7.2,
the project compiles fine.