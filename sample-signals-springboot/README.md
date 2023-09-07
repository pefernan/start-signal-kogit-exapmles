# org.kie.kogito.kogito-springboot-archetype - 0.1.3 #

# Running

- Compile and Run

    ```
    mvn clean package spring-boot:run    
    ```

# Test your application

Generated application comes with sample test process that allows you to verify if the application is working as expected. Simply execute following command to try it out

```sh
curl -d '{}' -H "Content-Type: application/json" -X POST http://localhost:8080/tests                                                                                                    
```

Once successfully invoked you should see "Hello World" in the console of the running application.

# Developing

Add your business assets resources (process definition, rules, decisions) into src/main/resources.

Add your java classes (data model, utilities, services) into src/main/java.

Then just build the project and run.


# Swagger documentation

Point to [swagger docs](http://localhost:8080/docs/swagger.json) to retrieve swagger definition of the exposed service

You can visualize that JSON file at [swagger editor](https://editor.swagger.io)

In addition client application can be easily generated from the swagger definition to interact with this service.

# Commands

Start instance of `startSignal` (String payload)

```shell
curl -X POST -H 'Content-Type:application/json' -H 'Accept:application/json' -d  'hello' http://localhost:8080/signalStart/start
```

Start instance of `signalStartObject` (`org.kie.kogito.Person` payload)

```shell
curl -X POST -H 'Content-Type:application/json' -H 'Accept:application/json' -d  '{"name": "Pere"}' http://localhost:8080/signalStartObject/start
```

Start instance of `signalStartEmpty` (**NO** payload)

```shell
 curl -X POST -H 'Content-Type:application/json' -H 'Accept:application/json' http://localhost:8080/signalStartEmpty/start   
```