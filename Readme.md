## Rest-Easy-Oclif-Plugin
or ... REOP

## This is a starting place, 
oclif finishes by generating a nodemodule / executable bin.

this repo is currently setup for planning and documentation.

the actual cli for this implementation will be in a different location labaled [here]().

## Acknowledgement
Inspiration comes from [John Hogarty](https://github.com/hogihung) and his project [rest easy](https://github.com/hogihung/rest_easy)

His project allows someone to test an api by creating a targets JSON file:
```json
  {
    "url_targets": [
      {
        "url": "http://localhost:9080/cloudmeta-api/v1/admin/status",
        "auth": "basic",
        "user": "cmadmin",
        "pass": "be3fcak3eat3rb3e328f05be0f7", 
        "label": "admin-status",
        "group": "cms-api"
      },
      {
        "url": "http://localhost:9080/cloudmeta-api/v1/hosts",
        "auth": "token",
        "token": "eyJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJwZW8tcGEiLCJ0eXAiOiJhY2Nlc3MiLCJuYW1lIjoiSm9obiBIb2dhcnR5IiwiZW1haWwiOiJqb2huLmhvZ2FydHlAb3JhY2xlLmNvbSIsImV4cCI6MTU1OTQwODI5MX0.b3IQmkg1RIQ3uNMiXhlmvsMK0EZbGEEReZR2VVU3kG4", 
        "label": "hosts",
        "group": "cms-api"
      }
    ]
  }
```

This projects aim is to generate as much of the targets.json file as possible.

By iterating all of an oclif cli's topics and find all commands.

![oclif-commands](https://user-images.githubusercontent.com/11463275/89427153-ec285d80-d708-11ea-827c-26930471035c.png)

It will also try to present all possible flags that can be used for the cli.

![flag-example](https://user-images.githubusercontent.com/11463275/89427158-edf22100-d708-11ea-962b-1a5dce2f94fc.png)

Lastly it will ask for 
1) external api's 
2) scenerio data

The hope is that the builder of the cli will be able to quickly test all of their endpoints if they came late to a project that did not implement testing or forgot to test along the way.
