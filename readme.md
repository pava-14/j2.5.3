# Задача № 3 "Внедряем стандарты кодирования"

## Краткое описание

1. Создан maven проект. 
2. Настроен CheckStyle plugin:

## Код

```
    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-checkstyle-plugin</artifactId>
        <version>3.1.1</version>
        <configuration>
            <configLocation>checkstyle.xml</configLocation>
            <encoding>UTF-8</encoding>
            <consoleOutput>true</consoleOutput>
            <failsOnError>true</failsOnError>
            <linkXRef>false</linkXRef>
            <configLocation>checkstyle.xml</configLocation>
        </configuration>
        <executions>
            <execution>
                <id>validate</id>
                <phase>verify</phase>
                <goals>
                    <goal>check</goal>
                </goals>
            </execution>
        </executions>
    </plugin>
```

## Лог
```
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running ru.netology.statistic.StatisticsServiceTest
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.03 s - in ru.netology.statistic.StatisticsServiceTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ statistics ---
[INFO] Building jar: C:\Users\79994\IdeaProjects\j2.5.3\target\statistics-1.0-SNAPSHOT.jar
[INFO] 
[INFO] --- maven-checkstyle-plugin:3.1.1:check (validate) @ statistics ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  12.226 s
[INFO] Finished at: 2020-05-24T16:57:06+07:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-checkstyle-plugin:3.1.1:check (validate) on project statistics: Failed during checkstyle execution: Failed during checkstyle configuration: unable to parse configuration stream - Element type "html" must be declared.:7:17 -> [Help 1]
org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.maven.plugins:maven-checkstyle-plugin:3.1.1:check (validate) on project statistics: Failed during checkstyle execution

```