# Задача № 3 "Внедряем стандарты кодирования"

## Краткое описание

1. Создан maven проект. 
2. Настроен SpotBugs plugin:

## Код

```
<dependencies>
  <dependency>
        <groupId>com.github.spotbugs</groupId>
        <artifactId>spotbugs-maven-plugin</artifactId>
        <version>4.0.0</version>
    </dependency>
</dependencies>

<plugin>
    <groupId>com.github.spotbugs</groupId>
    <artifactId>spotbugs-maven-plugin</artifactId>
    <version>4.0.0</version>
    <configuration>
        <effort>Max</effort>
        <threshold>Low</threshold>
        <xmlOutput>true</xmlOutput>
    </configuration>
    <executions>
        <execution>
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
[INFO] >>> spotbugs-maven-plugin:4.0.0:check (default) > :spotbugs @ statistics >>>
[INFO] 
[INFO] --- spotbugs-maven-plugin:4.0.0:spotbugs (spotbugs) @ statistics ---
[INFO] Fork Value is true
[INFO] Done SpotBugs Analysis....
[INFO] 
[INFO] <<< spotbugs-maven-plugin:4.0.0:check (default) < :spotbugs @ statistics <<<
[INFO] 
[INFO] 
[INFO] --- spotbugs-maven-plugin:4.0.0:check (default) @ statistics ---
[INFO] BugInstance size is 0
[INFO] Error size is 0
[INFO] No errors/warnings found
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  12.727 s
[INFO] Finished at: 2020-05-24T16:28:16+07:00
[INFO] ------------------------------------------------------------------------

```