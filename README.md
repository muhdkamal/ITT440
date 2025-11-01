Web Application Performance Testing 

NAME: MUHAMMAD KAMAL BIN OTHMAN

STUDENT ID: 2025118299

CLASS: M3CS2554C

TITLE: WEBSITE PERFORMANCE TESTING USING SIEGE 

Tool Selection Justification: Siege

Siege was selected as the testing tool for this performance analysis due to several reasons:

1. Open-Source Tool

Siege is an open-source tool, which is completely free to use without any fees.Siege also allows users 
to modify the code and customize it according to their specific needs. This tool also provide transparency 
and continuous improvement through contributions from developers around the world.

2. Support for HTTP and HTTPS Testing

Siege is primarily designed for testing HTTP and HTTPS-based web servers, which makes it very suitable 
for testing the performance of web applications and services. This allows it to simulate multiple users 
making requests to the web server, which is very suitable for several test like stress test, load test,
and spike test.

3. Lightweight and Efficient

Siege is a lightweight tool that does not require significant system resources to operate due to the use of 
command line (CLI) instead of Graphical User Interface (GUI). It is ideal for quick tests with minimum resource, 
and it can easily handle scenarios with a high number of concurrent users. Siege offers essential features such 
as customizable delays between requests to simulate realistic user behavior.

4. Ease of Use

Siege is known for its beginner-friendly concept and ease of use. The command-line interface (CLI) allows users to perform
specific tests by providing several basic parameters, such as the number of concurrent users, test duration, and 
the target URL. Additionally, the tool provides clear output, making it easy to analyze results.

TEST ENVIRONMENT SETUP AND METHADOLOGY

TESTED ENVIRONEMENT

IMAGE (KALI)
- Kali Linux is an open-source Linux distribution that is created for cybersecurity purpose. Even though it is closely
  related with cybersecurity, it is also can be used for other purposes, such as website's performance test in this case
  using 'siege' tool.

GUIDE:

1. Update the Kali Linux using above command
2. Install 'siege' using above command
3. run test using above command
   -c50 represent 50 users
   -t1M represents the test duration is 1 minute
   -specify the target website's URL
   
TESTED APPLICATION

https://tools-httpstatus.pickup-services.com/

This website is a public HTTP Status Code testing service that provides various endpoints to simulate server responses.
It is primarily designed for testing HTTP client behavior and verifying response codes such as 200 OK, 204 No Content, or 404 Not Found.
Due to it's lightweight feature, this website is suitable for quick performance and availability testing.

Key features include:

1. Simulation of standard HTTP response codes
2. Minimal payload responses for fast network benchmarking
3. Simple API endpoints suitable for automated or manual testing
4. Public accessibility without permission needed

Testing Infrastructure

This performance test was conducted using the following configuration:

Testing Tool: Siege 4.1.6
Operating System: Windows 11
System Memory: 32 GB RAM
Processor: AMD Ryzen 5 5600H
Network Connection: 131 Mbps mobile hotspot (may introduce variable latency)

Test Configuration

Performance Test Design

Objective: Evaluate the website’s response consistency and throughput under moderate concurrent user load in 1 minute.
Concurrent Users: 50 virtual users
Test Duration: 60 seconds (1 minute)
User Behavior: Accessed the root URL, which is 'https://tools-httpstatus.pickup-services.com/'.

HTTP Request Configuration

Protocol: HTTPS
Server Name: tools-httpstatus.pickup-services.com
Server URL: https://tools-httpstatus.pickup-services.com/
HTTP Method: GET
Port: 443

RAW DATA PRESENTATION

GRAPH1 IMAGE
Figure 1: Transaction Summary showing successful and failed transactions
GRAPH2 IMAGE
Figure 2: Key Performance Metrics Overview
GRAPH3 IMAGE
Figure 3: Transaction Time Comparison

INTERPRETATION OF RESULTS 

The performance test on the website https://tools-httpstatus.pickup-services.com/ shows that the site can handle response 
times well when there is a moderate load. The average response time of 2.69 seconds, as shown in the performance figure 1 graph.
This suggests that the server can manage multiple requests within a reasonable timeframe. Although the longest transaction recorded was 
19.18 seconds, this is still within an acceptable range for a public service that is under load, especially when dealing with 50 concurrent
users access the same website simultaneously. This indicates stable system performance for handling multiple user groups simultaneously.

The website is good at handling data, with a throughput rate of 0.21 MB/sec, as shown in Figure 2 graph. The transaction rate of 64.88
transactions per second shows that the server can manage multiple requests per second without serious problem, by maintaining the network 
utilization and server load. The total data transferred during the test was 12.35 MB, which shows that the website is efficiently handling 
resource usage while maintaining stable data transfer capabilities.

The website can also process a lot of transactions at once. It successfully processed 3909 transactions with a 98.99% availability rate,
even though 40 of them failed. This failure rate may be attributed to network timeouts or transient issues like rate limiting, which are 
common in publicly accessible testing endpoints. However, the overall result of 3909 successful transactions in just 60 seconds shows that
the server is capable of managing a massive volume of traffic without any serious problems.

BOTTLENECKS

The performance test on the website https://tools-httpstatus.pickup-services.com/ found a number of problems with the system's performance. 
The first bottleneck is the high average response time. Despite the website handling requests with consistent performance, the average response 
time recorded during the test was 2.69 seconds, which is a little bit high for users. Even though response times ranged from 0.77 seconds to 19.18 
seconds, the average response time of 2.69 seconds could cause noticeable delays for users especially in page loading, which is affecting user 
experience. The high response time could be attributed to factors such as network latency, server load, or traffic congestion.

The second bottleneck identified is the lack unknown system capacity limits. The test simulated 50 concurrent users, and the website handled these 
requests efficiently, with the success rate of 98.99%. However, because the website performed well under this load, we cannot determine its true capacity
limits. The cause of this limitation is the test configuration, which was not aggressive enough to push the system to its highest performance. 
In order to determine the exact breakpoint, higher user loads would be required in the future test.

The final bottleneck is only single-endpoint were used in this test. During the test, only a single endpoint, which is /GET, that was tested. In real-world 
scenarios, there will be several other endpoints like /POST, /PUT, AND /DELETE, which can add backend processing time. The backend processing times can vary 
across different request, and a variety of endpoints are often involved in serving different kinds of data. In our case, testing only one endpoint, which is
/GET, with a fixed load does not fully test the website's performance, especially on how the system will perform when handling more diverse traffic patterns. 
In practice, some requests might experience shorter response times, while others might take longer, especially under higher traffic loads or more complex process.
