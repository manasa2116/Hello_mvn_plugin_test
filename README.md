## Instructions
- Plugin can be invoked in 2 ways:
  - from the CLI following the standard - groupId:artifactId:version:goal
  - integrate it directly in one of the lifecycle phases of maven using the executions.execution pattern.

- Command to invoke the hello-maven-plugin
```
mvn com.lotusops:hello-maven-plugin:1.0.0-SNAPSHOT:sayhi
```

- Integrate in pom.xml
```
  <build>
    <plugins>
      <plugin>
        <groupId>com.lotusops</groupId>
        <artifactId>hello-maven-plugin</artifactId>
        <version>1.0.0-SNAPSHOT</version>
        <executions>
          <execution>
            <id>sayhi-id01</id>
            <phase>clean</phase>
            <goals>
              <goal>sayhi</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
    </plugins>
 </build>
```

## References
- https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html [Maven Lifecycle Phases]
- https://maven.apache.org/guides/mini/guide-configuring-plugins.html [Input to Maven Plugin]
