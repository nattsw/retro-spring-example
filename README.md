# barebones-spring

### Pre-req:
1. Put [Tomcat](https://tomcat.apache.org/download-80.cgi#8.5.8) somewhere 
(`/usr/local` or `/bin` or something)

### Setup:

1. Open the `pom.xml` file with IntelliJ (don't import/open project!)
1. Let IntelliJ download the internet for you
1. Install the `Tomcat and TomEE Integration` IntelliJ plugin (if haven't 
already)
1. Go to (⌘+Shift+A) `Edit Configurations...`
1. For `Application Server`, point IntelliJ to the location where the extracted
Tomcat was saved
1. Hit `+` and search for `Tomcat Server` (it's there, look harder!) then `Local`
1. Go to the `Deployment` tab then hit `+` to add an exploded artifact (See 
[this](http://stackoverflow.com/questions/1289358/what-does-exploded-development-mean-in-java) 
regarding explosiveness. Boomz)
1. Go back to `Server` tab and `On 'Update' action:` change the dropdown to 
`Update classes and resources` & hit OK

##### Run and profit

1. We should be able to see that `localhost:8080/hi` displays what was defined
in the controller
1. Take a look at the `WebInitializer.java` file to understand what's needed to
get the servlet up