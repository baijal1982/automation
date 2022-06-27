Sceanrio - Run Parallel test cases in selenium using docker hub in firefox and Chrome. 
view the same using VNC Viewer 


Steps

1. docker-compose -f ./docker-compose.yaml up

This will install selenium hub , chrome , edge , firefox and create a network. Also it will regster nodes with the hub .
once done , the smae can be seen at 
http://localhost:4444/ui

2. Run 
mvn clean test 
This will run the Test Suite in parallel in Chrome and Firefox . 

We are sending the test cases to hub. The hub is sending the same to Chrome and  Firefox instances.

3. Make a connection to vnc viewer as 
http://127.0.0.1:9001 - Chrome Password secret 
http://127.0.0.1:9002 - firefox  Password secret 


The test runs fine and can be viewed in vnc. 
