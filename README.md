# kie-server-client-request-body

## Prerequisites
- Maven (can be verified by running `mvn --version` from command line)
- Java 8 (or bigger, can be verified by running `java -version` from command line)

## Steps to prepare the request generator
- Clone or download this repository to your local machine
- Build it by invoking `mvn clean install` from location with pom.xml file
- Open any favourite Java IDE, import this project into it

## Steps to run the request generator
- Start Kie server which you want to use by client, configure it if needed (create containers...)
- Open KieServerRequestBodyGenerator in your IDE, edit Kie server URL, credentials and marshalling format as you need
- In case Kie server has disabled extensions comment out appropriate client initialization lines (see comments in file)
- In place marked by `*****` put your code which you want to examine for request/response, for example `kieServicesClient.createContainer("my-cont-id", new KieContainerResource(new ReleaseId("org.kie", "some-artifact", "1.0")));`
- Run the class as Java application (ideally from IDE)

After the application finishes check console output to see debug messages from Kie server. The request/response can be found in logs.
