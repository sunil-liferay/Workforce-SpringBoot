# Workforce-SpringBoot
Changes made to Workforce Applications.

### Instruction Noted ###
Change the configurations in "workforce\src\main\resources\application.properties" as per the local machine
(DB settings, server port, set the views, shut down configuration[implemented partially])

run "mvn clean install -DskipTests" through command prompt, from the "workforce" directory to build the war file

Right click "WorkforceApplication.java", run as java application

### Working URLs ###
http://localhost:9090/signup (registration)
http://localhost:9090/login (login)

### Observations ###
- Could not login in to system using the registered User
- Registered users are succesfully added to Database in Users table
- Use Sonarlint plugin of eclipse to format the code as per the sonar standards

### Kill the process the port ###
- Since applocation uses embedded tomcat, shutting tomcat down should be handled seperately, as a quick workaround use below things in command prompt

 netstat -ano | findstr :SERVERPORT  (SERVERPORT is serverport used in the properties file)
 taskkill /PID PROCESSID_FROM_ABOVE /F (PROCESSID_FROM_ABOVE is the ProcessID of the process, which is found in output of above command)
