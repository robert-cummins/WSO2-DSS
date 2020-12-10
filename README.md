# ${artifactId}

## Project Structure:
```
${artifactId}
   |___ ${artifactId}DSSConfig (ESB proxy services, sequences)
   |___ ${artifactId}DSSConfig_CAPP (ESB proxy services, sequences)
   |___ ${artifactId}ESBConfig (ESB proxy services, sequences)
   |___ ${artifactId}ESBConfig_CAPP (Composite Archive project for ESBConfig)          
   |___ ${artifactId}RegistryResources (Endpoints, XSD_Schema)
   |___ ${artifactId}RegistryResources_CAPP_DEV (Creates a CAR file containing DEV environment endpoints and schemas)
   |___ ${artifactId}RegistryResources_CAPP_SIT (Creates a CAR file containing SIT environment endpoints and schemas)
   |___ ${artifactId}RegistryResources_CAPP_EAT (Creates a CAR file containing EAT environment endpoints and schemas)
   |___ ${artifactId}RegistryResources_CAPP_SAND (Creates a CAR file containing SAND environment endpoints and schemas)
   |___ ${artifactId}RegistryResources_CAPP_PROD (Creates a CAR file containing PROD environment endpoints and schemas)
   |___ SOAPUI (SoapUI test resources)
   |___ Wiremock (Wiremock definitions for DEV environments)
```

| Project Details ||
| --- | --- |
| Service Name | ${artifactId} |
| Components | ESB, GREG |
| Design Documentation | http://www.onedatacom.com/client/MinistryofBIE/Operations/Middleware/ESB%202/ESB2%20Documentation/Application%20+%20Network%20Design%20Documents/${artifactId}/ |
| Business Group | Unknown |
| Business Owner | Unknown |
| Usage Type | Unknown |
| Service Type | REST |
| Development Vendor | Datacom |
| Development Contact | Shri Kant |
| API Store Group Name | N/A |
| Metadata/type of subscription | N/A |
| Inbound attachments | No |
| Outbound attachments | No |
| Typical Inbound Size | < 1KB |
| Typical Outbound Size | < 100KB |
| Estimated annual volume | Unknown |
| Datasource Configuration | N/A |
| DSS Rquired | No |
| B2B Queue Names | N/A |
| Regression Testing Url | TODO |

## UML
TODO

## Instructions
#### Import project into eclipse :
- Run ```$ mvn clean eclipse:eclipse ``` from ${artifactId} folder to generate eclipse project file.
- Import the projects using **Existing WSO2 projects to workspace** option in eclipse.

#### Build Instructions:
 - To generate Composite Archive (CAR) file
  ```
      $ mvn clean install
  ```

#### Deployment :
* Remove the previous version from ESB and Governance registry server.
  * From the carbon console, Use the following options to list the application deployed in the server ``` Home	 > Manage	 > Carbon Applications	 > List```
  * Select **delete** to undeploy the application(s).
* Deploy environment specific Registry-resource CAR file to Governance registry via carbon console.
  * For example, ${artifactId}RegistryResources_CAPP_DEV_1.0.0-SNAPSHOT.car should be deployed in DEV governance registry server.
* Deploy ESBConfig CAR file (${artifactId}ESBConfig_CAPP_1.0.0-SNAPSHOT.car) to ESB server via carbon console.# WSO2-DSS
