# JMH sample from jmh archetype

```bash
#Step 1
mvn archetype:generate \
  -DinteractiveMode=false \
  -DarchetypeGroupId=org.openjdk.jmh \
  -DarchetypeArtifactId=jmh-java-benchmark-archetype \
  -DgroupId=org.sample \
  -DartifactId=test \
  -Dversion=1.0

# Step 2 
cd test/
mvn clean verify

# Step 3
java -jar target/benchmarks.jar

Exception in thread "main" java.lang.RuntimeException: ERROR: Unable to find the resource: /META-INF/BenchmarkList
        at org.openjdk.jmh.runner.AbstractResourceReader.getReaders(AbstractResourceReader.java:98)
        at org.openjdk.jmh.runner.BenchmarkList.find(BenchmarkList.java:124)
        at org.openjdk.jmh.runner.Runner.internalRun(Runner.java:252)
        at org.openjdk.jmh.runner.Runner.run(Runner.java:208)
        at org.openjdk.jmh.Main.main(Main.java:71)

java -version
openjdk version "24.0.1" 2025-04-15
OpenJDK Runtime Environment GraalVM CE 24.0.1+9.1 (build 24.0.1+9-jvmci-b01)
OpenJDK 64-Bit Server VM GraalVM CE 24.0.1+9.1 (build 24.0.1+9-jvmci-b01, mixed mode, sharing)
```

## References

- https://github.com/openjdk/jmh