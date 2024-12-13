# Simple Rest controller Demo App
The embedded server should be responding to a local http Get request with a simple text on the screen. 

## Set Up
1. Create project dependencies with [initializr](https://start.spring.io/).
   - Project: Maven
   - Language: Java
   - Spring Boot: 3.4.0 
   - Project Metadata: ...
   - Packaging: Jar
   - Java: 21
   - Dependencies: "Spring Web"
2. Generate zip file and unpack in IDE.
   
## Implementation
1. Create a package for the "rest controller".
2. Add a class with the following code:  
```java
@RestController
public class SimpleRestController {
    
    @GetMapping("/")                    // expose "/" that return "Hello World"
    public String sayHello(){           // method to be called
        return "Hello World";           // string to be returned
    }
}
```

## Execution
1. Start the application (*play button in HttpEndpointDemoApplication.java*).
2. Tomcat server should be starting on port `8080`
3. Open the browser, enter `http://localhost:8080/` the url address.
4. The returned page should display the text `Hello World`.