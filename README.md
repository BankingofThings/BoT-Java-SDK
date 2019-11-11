# BoT-Java-SDK
    Finn BoT SDK to interact with Banking of things Service using Java programming language to enable 
    IoT devices with autonomous payments.
    
## Prerequisites
* **Hardware Devices**
  - [Raspberry Pi](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up/2)
  - Systems running Mac OS, Linux and Windows
  
* **Software Tools**
  - [JDK](https://www.raspberrypi.org/blog/oracle-java-on-raspberry-pi/)
  - [Apache Maven](https://maven.apache.org/)
  - [Redis](https://redis.io/)
  - [Node JS](https://nodejs.org/en/)
  - [Git](https://projects.raspberrypi.org/en/projects/getting-started-with-git/4)
  
 ## Build
 * Clone the project using `git` or Download the BoT-Java-SDK.zip and extract
 * Go to BoT-Java-SDK directory
 * Execute the command `mvn clean package`
 * On successful build completion, find `BoT-Java-SDK.jar` in the path `BoT-Java-SDK/target`
 
 ## Execution
 * We need 2 prerequisite setup files to be copied to the directory from where needs to be `BoT-Java-SDK.jar`
   - Copy `logback.xml` from the path `BoT-Java-SDK/src/main/resources` to the execution directory
   - Copy `bleno-service.js` from the path `BoT-Java-SDK/src/main/resources` to the execution directory
 * Make sure `redis-server` is up and running before executing the `BoT-Java-SDK.jar`
 * To bootstrap the webserver and consume the ReST endpoints, execute the command `java -jar BoT-Java-SDK.jar server`
   - The available end points to consume are /qrcode   /actions   /pairing
   - The server log can be found at the location `/tmp/BoT-Java-SDK-Webserver.log`
 * To run the library sample, execute the command `java -jar BoT-Java-SDK.jar libSample`
