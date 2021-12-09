# Maven-module
Sample Project show how use springBoot and maven to create module and use spring-boot as dependencyManagement

## command:
1 - for create maven basic parent-module:
```
mvn archetype:generate 
    -DgroupId=com.yourdomain.project 
    -DartifactId=your-app 
    -DarchetypeArtifactId=maven-archetype-quickstart  
    -DarchetypeVersion=1.4 -DinteractiveMode=false
```

2 - remove src folder <br>
3 - create child maven module into project and added to parent pom <br>
```  
<modules>
    <module>childmodule</module>
</modules>
```
4 - define parent module in child module <br>
```    
<parent>
    <artifactId>samplemodule</artifactId>
    <groupId>ir.bigz</groupId>
    <version>1.0-SNAPSHOT</version>
</parent>
```

