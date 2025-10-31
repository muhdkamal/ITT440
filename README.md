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


