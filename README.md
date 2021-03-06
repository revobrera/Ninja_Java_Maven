Using Ninja Framework, Java, Maven & Cloud9 
================

##Evironment Setup
Setting up the environment can be the most tedious and sometimes the first milestone to getting things started. If the environment doesn't work properly the first time, it will take some troubleshooting to get over the hurdle. Here are straight forward instructions to getting everything all set up!

1. Navigate to your Cloud9 and create a new project
2. Java is setup already in C9 - check the version and type in the command line: `java -version`

  ```command
  java version "1.7.0_65"
  OpenJDK Runtime Environment (IcedTea 2.5.3) (7u71-2.5.3-0ubuntu0.14.04.1)
  OpenJDK 64-Bit Server VM (build 24.65-b04, mixed mode)
  ```
3. Maven is setup already in C9 - check the version and type in the command line: `mvn -version` 

  ```command
  Apache Maven 2.2.1 (rdebian-14)
  Java version: 1.7.0_65
  Java home: /usr/lib/jvm/java-7-openjdk-amd64/jre
  Default locale: en, platform encoding: UTF-8
  OS name: "linux" version: "3.14.13-c9" arch: "amd64" Family: "unix"
  ```
  
4. Then we look if our versions are compatible with the [Ninja Framework](http://www.ninjaframework.org/documentation/getting_started/installing_ninja.html).
We can see that the versions required for Maven is 3 or greater. So we need to remove the current installation of Maven 2 and install a fresh version of Maven 3.

5. Remove Maven 2.2.1 by typeing in the command line: `sudo apt-get remove maven2`
  
  ```command
  Reading package lists... Done
  Building dependency tree       
  Reading state information... Done
  The following packages were automatically installed and are no longer required:
    junit4 libantlr-java libasm3-java libatinject-jsr330-api-java
    libclassworlds-java libcommons-beanutils-java libcommons-cli-java
    libcommons-codec-java libcommons-collections3-java
    libcommons-configuration-java libcommons-digester-java
    libcommons-httpclient-java libcommons-jexl2-java libcommons-jxpath-java
    libcommons-lang-java libcommons-net2-java libcommons-validator-java
    libcommons-vfs-java libdoxia-java libdoxia-sitetools-java libeasymock-java
    libganymed-ssh2-java libguava-java libhamcrest-java libhttpclient-java
    libhttpcore-java libitext1-java libjdependency-java libjetty-java
    libjsoup-java libjsr305-java libjtidy-java libmaven-archiver-java
    libmaven-clean-plugin-java libmaven-compiler-plugin-java
    libmaven-dependency-tree-java libmaven-filtering-java
    libmaven-install-plugin-java libmaven-jar-plugin-java
    libmaven-plugin-tools-java libmaven-reporting-impl-java
    libmaven-resources-plugin-java libmaven-scm-java libmaven-shade-plugin-java
    libmaven2-core-java libmodello-java libnetbeans-cvsclient-java
    libplexus-ant-factory-java libplexus-archiver-java
    libplexus-bsh-factory-java libplexus-build-api-java libplexus-cipher-java
    libplexus-classworlds-java libplexus-compiler-java
    libplexus-container-default-java libplexus-containers-java
    libplexus-digest-java libplexus-i18n-java libplexus-interactivity-api-java
    libplexus-interpolation-java libplexus-io-java libplexus-sec-dispatcher-java
    libplexus-utils-java libplexus-velocity-java libqdox-java libservlet2.5-java
    libslf4j-java libwagon-java libwerken.xpath-java libxbean-java velocity
  Use 'apt-get autoremove' to remove them.
  The following packages will be REMOVED:
    maven2
  0 upgraded, 0 newly installed, 1 to remove and 1 not upgraded.
  After this operation, 2322 kB disk space will be freed.
  Do you want to continue? [Y/n] Y
  (Reading database ... 123544 files and directories currently installed.)
  Removing maven2 (2.2.1-19) ...
  ```
6. Install latest version of Maven by typing in the command line: `sudo apt-get install maven`

  ```command
  Reading package lists... Done
  Building dependency tree       
  Reading state information... Done
  The following packages were automatically installed and are no longer required:
    libantlr-java libcommons-validator-java libdoxia-sitetools-java
    libjdependency-java libjtidy-java libmaven-archiver-java
    libmaven-clean-plugin-java libmaven-compiler-plugin-java
    libmaven-dependency-tree-java libmaven-filtering-java
    libmaven-install-plugin-java libmaven-jar-plugin-java
    libmaven-plugin-tools-java libmaven-reporting-impl-java
    libmaven-resources-plugin-java libmaven-shade-plugin-java
    libplexus-compiler-java libplexus-digest-java libplexus-velocity-java
    libwerken.xpath-java velocity
  Use 'apt-get autoremove' to remove them.
  The following extra packages will be installed:
    aspectj libaether-java libaopalliance-java libaspectj-java
    libasync-http-client-java libcdi-api-java libcglib-java
    libgeronimo-interceptor-3.0-spec-java libgeronimo-jpa-2.0-spec-java
    libgeronimo-osgi-support-java libguice-java libjackrabbit-java
    libjcommander-java libmaven-parent-java libnetty-java
    libosgi-compendium-java libosgi-core-java libosgi-foundation-ee-java
    libplexus-classworlds2-java libplexus-cli-java libplexus-containers1.5-java
    libplexus-utils2-java libsisu-guice-java libsisu-ioc-java libwagon2-java
    libyaml-snake-java testng
  Suggested packages:
    libaopalliance-java-doc libasync-http-client-java-doc
    libgeronimo-jpa-2.0-spec-java-doc libgeronimo-osgi-support-java-doc
    libjcommander-java-doc libosgi-compendium-java-doc libosgi-core-java-doc
    libosgi-foundation-ee-java-doc libplexus-classworlds2-java-doc
    libplexus-cli-java-doc libplexus-utils2-java-doc
  The following NEW packages will be installed:
    aspectj libaether-java libaopalliance-java libaspectj-java
    libasync-http-client-java libcdi-api-java libcglib-java
    libgeronimo-interceptor-3.0-spec-java libgeronimo-jpa-2.0-spec-java
    libgeronimo-osgi-support-java libguice-java libjackrabbit-java
    libjcommander-java libmaven-parent-java libnetty-java
    libosgi-compendium-java libosgi-core-java libosgi-foundation-ee-java
    libplexus-classworlds2-java libplexus-cli-java libplexus-containers1.5-java
    libplexus-utils2-java libsisu-guice-java libsisu-ioc-java libwagon2-java
    libyaml-snake-java maven testng
  0 upgraded, 28 newly installed, 0 to remove and 1 not upgraded.
  Need to get 20.3 MB of archives.
  After this operation, 25.9 MB of additional disk space will be used.
  Do you want to continue? [Y/n] Y
  Get:1 http://archive.ubuntu.com/ubuntu/ trusty/universe libyaml-snake-java all 1.12-2 [244 kB]
  Get:2 http://archive.ubuntu.com/ubuntu/ trusty/universe libaspectj-java all 1.6.12+dfsg-3 [11.1 MB]
  Get:3 http://archive.ubuntu.com/ubuntu/ trusty/universe aspectj all 1.6.12+dfsg-3 [19.3 kB]
  Get:4 http://archive.ubuntu.com/ubuntu/ trusty/universe libnetty-java all 1:3.2.6.Final-2 [671 kB]
  Get:5 http://archive.ubuntu.com/ubuntu/ trusty/universe libasync-http-client-java all 1.6.5-2 [311 kB]
  Get:6 http://archive.ubuntu.com/ubuntu/ trusty/universe libplexus-classworlds2-java all 2.5.1-2 [46.6 kB]
  Get:7 http://archive.ubuntu.com/ubuntu/ trusty/universe libplexus-cli-java all 1.2-5 [9700 B]
  Get:8 http://archive.ubuntu.com/ubuntu/ trusty/universe libplexus-utils2-java all 2.0.5-1 [214 kB]
  Get:9 http://archive.ubuntu.com/ubuntu/ trusty/universe libplexus-containers1.5-java all 1.5.5-6 [293 kB]
  Get:10 http://archive.ubuntu.com/ubuntu/ trusty/universe libaopalliance-java all 20070526-5 [9214 B]
  Get:11 http://archive.ubuntu.com/ubuntu/ trusty/universe libgeronimo-interceptor-3.0-spec-java all 1.0.1-1fakesync1 [5132 B]
  Get:12 http://archive.ubuntu.com/ubuntu/ trusty/universe libcdi-api-java all 1.0-1 [32.7 kB]
  Get:13 http://archive.ubuntu.com/ubuntu/ trusty/universe libsisu-guice-java all 3.1.1+dfsg-1 [550 kB]
  Get:14 http://archive.ubuntu.com/ubuntu/ trusty/universe libsisu-ioc-java all 2.3.0-5 [458 kB]
  Get:15 http://archive.ubuntu.com/ubuntu/ trusty/universe libaether-java all 1.13.1-2 [496 kB]
  Get:16 http://archive.ubuntu.com/ubuntu/ trusty/main libcglib-java all 2.2.2+dfsg-5 [710 kB]
  Get:17 http://archive.ubuntu.com/ubuntu/ trusty/universe libosgi-core-java all 4.3.0-4 [93.1 kB]
  Get:18 http://archive.ubuntu.com/ubuntu/ trusty/universe libosgi-foundation-ee-java all 4.2.0-1 [336 kB]
  Get:19 http://archive.ubuntu.com/ubuntu/ trusty/universe libosgi-compendium-java all 4.3.0-1 [383 kB]
  Get:20 http://archive.ubuntu.com/ubuntu/ trusty/universe libgeronimo-osgi-support-java all 1.0-2 [17.9 kB]
  Get:21 http://archive.ubuntu.com/ubuntu/ trusty/universe libgeronimo-jpa-2.0-spec-java all 1.1-2 [81.8 kB]
  Get:22 http://archive.ubuntu.com/ubuntu/ trusty/universe libguice-java all 3.0-3 [488 kB]
  Get:23 http://archive.ubuntu.com/ubuntu/ trusty/universe libjackrabbit-java all 2.3.6-1 [277 kB]
  Get:24 http://archive.ubuntu.com/ubuntu/ trusty/universe libjcommander-java all 1.32-1 [55.5 kB]
  Get:25 http://archive.ubuntu.com/ubuntu/ trusty/universe libmaven-parent-java all 21-2 [5786 B]
  Get:26 http://archive.ubuntu.com/ubuntu/ trusty/universe libwagon2-java all 2.5-1 [1278 kB]
  Get:27 http://archive.ubuntu.com/ubuntu/ trusty/universe maven all 3.0.5-1 [1303 kB]
  Get:28 http://archive.ubuntu.com/ubuntu/ trusty/universe testng all 6.8.7-2 [767 kB]
  Fetched 20.3 MB in 2s (9602 kB/s)
  Selecting previously unselected package libyaml-snake-java.
  (Reading database ... 123528 files and directories currently installed.)
  Preparing to unpack .../libyaml-snake-java_1.12-2_all.deb ...
  Unpacking libyaml-snake-java (1.12-2) ...
  Selecting previously unselected package libaspectj-java.
  Preparing to unpack .../libaspectj-java_1.6.12+dfsg-3_all.deb ...
  Unpacking libaspectj-java (1.6.12+dfsg-3) ...
  Selecting previously unselected package aspectj.
  Preparing to unpack .../aspectj_1.6.12+dfsg-3_all.deb ...
  Unpacking aspectj (1.6.12+dfsg-3) ...
  Selecting previously unselected package libnetty-java.
  Preparing to unpack .../libnetty-java_1%3a3.2.6.Final-2_all.deb ...
  Unpacking libnetty-java (1:3.2.6.Final-2) ...
  Selecting previously unselected package libasync-http-client-java.
  Preparing to unpack .../libasync-http-client-java_1.6.5-2_all.deb ...
  Unpacking libasync-http-client-java (1.6.5-2) ...
  Selecting previously unselected package libplexus-classworlds2-java.
  Preparing to unpack .../libplexus-classworlds2-java_2.5.1-2_all.deb ...
  Unpacking libplexus-classworlds2-java (2.5.1-2) ...
  Selecting previously unselected package libplexus-cli-java.
  Preparing to unpack .../libplexus-cli-java_1.2-5_all.deb ...
  Unpacking libplexus-cli-java (1.2-5) ...
  Selecting previously unselected package libplexus-utils2-java.
  Preparing to unpack .../libplexus-utils2-java_2.0.5-1_all.deb ...
  Unpacking libplexus-utils2-java (2.0.5-1) ...
  Selecting previously unselected package libplexus-containers1.5-java.
  Preparing to unpack .../libplexus-containers1.5-java_1.5.5-6_all.deb ...
  Unpacking libplexus-containers1.5-java (1.5.5-6) ...
  Selecting previously unselected package libaopalliance-java.
  Preparing to unpack .../libaopalliance-java_20070526-5_all.deb ...
  Unpacking libaopalliance-java (20070526-5) ...
  Selecting previously unselected package libgeronimo-interceptor-3.0-spec-java.
  Preparing to unpack .../libgeronimo-interceptor-3.0-spec-java_1.0.1-1fakesync1_all.deb ...
  Unpacking libgeronimo-interceptor-3.0-spec-java (1.0.1-1fakesync1) ...
  Selecting previously unselected package libcdi-api-java.
  Preparing to unpack .../libcdi-api-java_1.0-1_all.deb ...
  Unpacking libcdi-api-java (1.0-1) ...
  Selecting previously unselected package libsisu-guice-java.
  Preparing to unpack .../libsisu-guice-java_3.1.1+dfsg-1_all.deb ...
  Unpacking libsisu-guice-java (3.1.1+dfsg-1) ...
  Selecting previously unselected package libsisu-ioc-java.
  Preparing to unpack .../libsisu-ioc-java_2.3.0-5_all.deb ...
  Unpacking libsisu-ioc-java (2.3.0-5) ...
  Selecting previously unselected package libaether-java.
  Preparing to unpack .../libaether-java_1.13.1-2_all.deb ...
  Unpacking libaether-java (1.13.1-2) ...
  Selecting previously unselected package libcglib-java.
  Preparing to unpack .../libcglib-java_2.2.2+dfsg-5_all.deb ...
  Unpacking libcglib-java (2.2.2+dfsg-5) ...
  Selecting previously unselected package libosgi-core-java.
  Preparing to unpack .../libosgi-core-java_4.3.0-4_all.deb ...
  Unpacking libosgi-core-java (4.3.0-4) ...
  Selecting previously unselected package libosgi-foundation-ee-java.
  Preparing to unpack .../libosgi-foundation-ee-java_4.2.0-1_all.deb ...
  Unpacking libosgi-foundation-ee-java (4.2.0-1) ...
  Selecting previously unselected package libosgi-compendium-java.
  Preparing to unpack .../libosgi-compendium-java_4.3.0-1_all.deb ...
  Unpacking libosgi-compendium-java (4.3.0-1) ...
  Selecting previously unselected package libgeronimo-osgi-support-java.
  Preparing to unpack .../libgeronimo-osgi-support-java_1.0-2_all.deb ...
  Unpacking libgeronimo-osgi-support-java (1.0-2) ...
  Selecting previously unselected package libgeronimo-jpa-2.0-spec-java.
  Preparing to unpack .../libgeronimo-jpa-2.0-spec-java_1.1-2_all.deb ...
  Unpacking libgeronimo-jpa-2.0-spec-java (1.1-2) ...
  Selecting previously unselected package libguice-java.
  Preparing to unpack .../libguice-java_3.0-3_all.deb ...
  Unpacking libguice-java (3.0-3) ...
  Selecting previously unselected package libjackrabbit-java.
  Preparing to unpack .../libjackrabbit-java_2.3.6-1_all.deb ...
  Unpacking libjackrabbit-java (2.3.6-1) ...
  Selecting previously unselected package libjcommander-java.
  Preparing to unpack .../libjcommander-java_1.32-1_all.deb ...
  Unpacking libjcommander-java (1.32-1) ...
  Selecting previously unselected package libmaven-parent-java.
  Preparing to unpack .../libmaven-parent-java_21-2_all.deb ...
  Unpacking libmaven-parent-java (21-2) ...
  Selecting previously unselected package libwagon2-java.
  Preparing to unpack .../libwagon2-java_2.5-1_all.deb ...
  Unpacking libwagon2-java (2.5-1) ...
  Selecting previously unselected package maven.
  Preparing to unpack .../archives/maven_3.0.5-1_all.deb ...
  Unpacking maven (3.0.5-1) ...
  Selecting previously unselected package testng.
  Preparing to unpack .../testng_6.8.7-2_all.deb ...
  Unpacking testng (6.8.7-2) ...
  Processing triggers for man-db (2.6.7.1-1ubuntu1) ...
  Setting up libyaml-snake-java (1.12-2) ...
  Setting up libaspectj-java (1.6.12+dfsg-3) ...
  Setting up aspectj (1.6.12+dfsg-3) ...
  Setting up libnetty-java (1:3.2.6.Final-2) ...
  Setting up libasync-http-client-java (1.6.5-2) ...
  Setting up libplexus-classworlds2-java (2.5.1-2) ...
  Setting up libplexus-cli-java (1.2-5) ...
  Setting up libplexus-utils2-java (2.0.5-1) ...
  Setting up libplexus-containers1.5-java (1.5.5-6) ...
  Setting up libaopalliance-java (20070526-5) ...
  Setting up libgeronimo-interceptor-3.0-spec-java (1.0.1-1fakesync1) ...
  Setting up libcdi-api-java (1.0-1) ...
  Setting up libsisu-guice-java (3.1.1+dfsg-1) ...
  Setting up libsisu-ioc-java (2.3.0-5) ...
  Setting up libaether-java (1.13.1-2) ...
  Setting up libcglib-java (2.2.2+dfsg-5) ...
  Setting up libosgi-core-java (4.3.0-4) ...
  Setting up libosgi-foundation-ee-java (4.2.0-1) ...
  Setting up libguice-java (3.0-3) ...
  Setting up libjackrabbit-java (2.3.6-1) ...
  Setting up libjcommander-java (1.32-1) ...
  Setting up libmaven-parent-java (21-2) ...
  Setting up libwagon2-java (2.5-1) ...
  Setting up maven (3.0.5-1) ...
  update-alternatives: using /usr/share/maven/bin/mvn to provide /usr/bin/mvn (mvn) in auto mode
  Setting up testng (6.8.7-2) ...
  Setting up libosgi-compendium-java (4.3.0-1) ...
  Setting up libgeronimo-osgi-support-java (1.0-2) ...
  Setting up libgeronimo-jpa-2.0-spec-java (1.1-2) ...
  ```
7. Great! You have successfully set up your environment! 

###Congratulations! You did it!

##Maven Archetypes
These archetypes are blueprints that create the entire project structure. You will need to follow the following instructions to generate your files/folders. 

  ```command
  mvn archetype:generate -DarchetypeGroupId=org.ninjaframework -DarchetypeArtifactId=ninja-servlet-archetype-simple
  ```
It will then download necessary dependencies and needed files. Maven will then ask to configure your project. Here's an example of mine:

  ```command
  Define value for property 'groupId': : org.gizmoose.ninjaven
  Define value for property 'artifactId': : ninjaven
  Define value for property 'version':  1.0-SNAPSHOT: : 0.1.0
  Define value for property 'package':  org.gizmoose.ninjaven: : org.gizmoose.ninjaven:
  ```
You will then be asked to confirm to build the project:

  ```command
  Confirm properties configuration:
  groupId: org.gizmoose.ninjaven
  artifactId: ninjaven
  version: 0.1.0
  package: org.gizmoose.ninjaven:
   Y: : 
  [INFO] ----------------------------------------------------------------------------
  [INFO] Using following parameters for creating project from Archetype: ninja-servlet-archetype-simple:4.0.2
  [INFO] ----------------------------------------------------------------------------
  [INFO] Parameter: groupId, Value: org.gizmoose.ninjaven
  [INFO] Parameter: artifactId, Value: ninjaven
  [INFO] Parameter: version, Value: 0.1.0
  [INFO] Parameter: package, Value: org.gizmoose.ninjaven:
  [INFO] Parameter: packageInPathFormat, Value: org/gizmoose/ninjaven:
  [INFO] Parameter: package, Value: org.gizmoose.ninjaven:
  [INFO] Parameter: version, Value: 0.1.0
  [INFO] Parameter: groupId, Value: org.gizmoose.ninjaven
  [INFO] Parameter: artifactId, Value: ninjaven
  [INFO] project created from Archetype in dir: /home/ubuntu/workspace/ninjaven
  [INFO] ------------------------------------------------------------------------
  [INFO] BUILD SUCCESS
  [INFO] ------------------------------------------------------------------------
  [INFO] Total time: 6:43.496s
  [INFO] Finished at: Sat Dec 20 01:05:12 UTC 2014
  [INFO] Final Memory: 15M/907M
  [INFO] ------------------------------------------------------------------------
  ```
After completing the generation, execute the following commands:

  ```command
  cd ninjaven
  ```
To generate the compiled classes for the first time:

  ```command
  mvn clean install
  ```
NOTE: A significant part of MAVEN is the use of repositories to manage jar files across different projects.
Set up JAVA_HOME in Cloud9:

1. cd to `/home` folder
2. `vi .bash_aliases` 
3. In the vi editor, navigate the cursor to the last line.
4. Type `a` to start appending text after the cursor.
5. Type in a new line, `alias JAVA_HOME=usr/lib/jvm/java-1.7.0-openjdk-amd64`
6. Press the `Esc` key
7. 7. Type `ZZ` to exit and save changes.


  ```command
  
  ```

To start Ninja's SuperDevMode:

  ```command
  mvn ninja:run
  ```
