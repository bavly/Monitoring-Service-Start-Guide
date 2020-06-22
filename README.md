# Monitoring Service Start Guide

Some points you need to start think about it, before Monitoring your service.

- We have 2 Layers      from Server layer ( Linux , windows ) , Application layer 
- We will be talk about these 2 layers 

# First we will talk about Server layer. 
- from server perspective I think Zabbix (https://www.zabbix.com/) Free open source monitoring service, will be enough for you to monitor the server. 

# Second we will talk about Application layer. 

- There are some questions :- 

- What is the scale of the application ?
- Do you deploy on 2 servers only or on horizontal scalling you are increasing number of servers resource ?
- Do you use to deploy on Kubernates & Docker ? 

# To answer these questions, check the following below should be a good start.

1 - Think of the monitoring application layer like , you are in jungle, you must trace your feet when you walk, as when you ever need to return back, be easy for you 
(that is what the monitoring service should do, must know your start & how you return back from perviouse step )

2 - integration with third party APIs (how long it takes , timeout) If external interaction fails, what will be behavior of the application?

3 - if enternal requests ( to follow the chain of request simply in nginX they generate request ID so that you could forword this ID in the all chain of the request inorder to follow & check the request what is )

4 - Think of failure Scenrios :- 
    Example like order is down how to know & where is the start to check it (Alert before it happened Alert on number of connections in Database, Alert on request queing increase , error rate increase on 10% alert if increasing to check it) 

5- Almost Alert on every service when it is down, Do not wait for bussiness to let you know.

6- Must know when API fails, when it is working ?

7- Learn about ELK stack to Analyis monitoring Log system. https://www.elastic.co/what-is/elk-stack 

8- If the bussiness needs Dashbord for new service, on going services 
   Do not think about save these data in Database will be hassel for you to mange it, every time or 1 hour 
   There are some services doing that like 
   https://www.datadoghq.com/ ,  https://newrelic.com/

