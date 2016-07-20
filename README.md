# checkstyle-configuration
Contains Checkstyle configurations for Viskan projects.

## Usage
```xml
    ...
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-checkstyle-plugin</artifactId>
            <version>2.17</version>
            <dependencies>
                <dependency>
                    <groupId>com.viskan</groupId>
                    <artifactId>checkstyle-configuration</artifactId>
                    <version>3</version>
                </dependency>
                <dependency>
                    <groupId>com.puppycrawl.tools</groupId>
                    <artifactId>checkstyle</artifactId>
                    <version>6.19</version>
                </dependency>
            </dependencies>
            <executions>
                <execution>
                    <id>checkstyle-main</id>
                    <goals>
                        <goal>check</goal>
                    </goals>
                    <configuration>
                        <sourceDirectories>
                            <sourceDirectory>src/main/java/</sourceDirectory>
                        </sourceDirectories>
                        <includeResources>true</includeResources>
                        <includeTestResources>false</includeTestResources>
                        <configLocation>viskan-checkstyle-main.xml</configLocation>
                        <violationSeverity>warning</violationSeverity>
                    </configuration>
                </execution>
                    <execution>
                    <id>checkstyle-test</id>
                    <goals>
                        <goal>check</goal>
                    </goals>
                    <configuration>
                        <sourceDirectories>
                            <sourceDirectory>src/test/java/</sourceDirectory>
                        </sourceDirectories>
                        <includeResources>false</includeResources>
                        <includeTestResources>true</includeTestResources>
                        <configLocation>viskan-checkstyle-test.xml</configLocation>
                        <violationSeverity>warning</violationSeverity>
                    </configuration>
                </execution>
            </executions>
        </plugin>
    </plugins>
    ...
```

## License
Apache License 2.0 © [Viskan Distanshandel System AB](http://viskan.com/)
