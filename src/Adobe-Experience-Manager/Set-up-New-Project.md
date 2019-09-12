## Project Setup

- Paste the following command [in your preferred CLI] to initiate the creation of new project.
  
  > ```Assembly
  > mvn org.apache.maven.plugins:maven-archetype-plugin:2.4:generate \
  > -DarchetypeGroupId=com.adobe.granite.archetypes \
  > -DarchetypeArtifactId=aem-project-archetype \
  > -DarchetypeVersion=13 \
  > -DarchetypeCatalog=https://repo.adobe.com/nexus/content/groups/public/

- CLI will ask series of questions to setup the project:
  > ```Assembly
  > Define value for property 'groupId':
  > Define value for property 'version' 1.0-SNAPSHOT: : 
  > Define value for property 'package':
  > Define value for property 'appsFolderName':
  > Define value for property 'artifactId':
  > Define value for property 'artifactName': 
  > Define value for property 'componentGroupName': 
  > Define value for property 'confFolderName': 
  > Define value for property 'contentFolderName': 
  > Define value for property 'cssId': 
  > Define value for property 'packageGroup': 
  > Define value for property 'siteName': 

- Folder and File structure will be generated as below:  
  > ```Assembly
  > ├── <artifactName>
  >     ├── core/
  >     ├── it.launcher/
  >     ├── it.tests/
  >     ├── pom.xml
  >     ├── README.md
  >     ├── ui.apps/
  >     └── ui.content/
   
  - __core__: contains Java code, ie. schedulers, servlets, components-based Java code etc.
  - __pom.xml__: manage dependency and deploy maven bundles
  - __it.tests__: contains unit test
  - __it.launcher__: deploys `it.tests` to the server
  - __ui.apps__: contains `/apps` part of the project, ie. components, client libraries, templates, etc.
  - __ui.content__: contains structural content (/content)
  
## Maven Profile

<dl>
  <dt>mvn clean</dt>
  <dd></dd>
  <dt>mvn clean install</dt>
  <dd></dd>
  <dt>mvn clean install -PautoInstallPackage</dt>
  <dd></dd>
  <dt>mvn clean install -PautoInstallContent</dt>
  <dd></dd>
  <dt>mvn clean install -PautoInstallPackagePublish</dt>
  <dd></dd>
</dl>
