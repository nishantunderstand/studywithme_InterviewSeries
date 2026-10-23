

APM stands for Application Performance Monitoring (sometimes also called Application Performance Management).

Yes, Datadog and New Relic can measure API response time, show p95/p99 latency, and help you investigate slow requests using distributed traces.

## 1. How do we test API response time?

There are three common approaches:

| Approach       | Tool                          | Purpose                                                          |
| -------------- | ----------------------------- | ---------------------------------------------------------------- |
| Manual testing | Postman                       | Check an individual API's response time                          |
| Load testing   | JMeter, k6                    | Measure response time under concurrent traffic                   |
| APM monitoring | Datadog, New Relic, Dynatrace | Monitor live application performance and investigate bottlenecks |

![API response structure in Postman | Postman Docs](https://images.openai.com/static-rsc-4/XkyGWeXePsMnzt67AyXyj_jU4aTbha2bx4QVcRVaXP-fz-nt6bFu23cH5ZPt6-Bo8PDUyBbIeutQLtiQL23dVkkrFTyF_WkbGV2j7VF2eGMT8_DqmRbm0syEq98neZwNg88ZighLV1rCfl4njKCpFHjRFXJ1wQRViC7IK6pQz0w?purpose=inline)

1. Postman

Send a request and check the response time shown in the response panel. Good for quick, individual API tests.

![快速生成测试报告：JMeter 测试教程](https://images.openai.com/static-rsc-4/emGzsujWjUABa82X2HE5KVRFdJ7_BckdhsITyPJvuRJnBhJTQDfe9nRqKNgHLcL2PI1fO3IQSE53lY4f2wAgZH07YbsQRLdyd5WuOj0wzx0FGrFKdCBfS1uyiqnAKZJBKLZuJdxaeDzoOkQINfl_3FRDqtinTSWBLFQzcPAGkGQ?purpose=inline)

2. Apache JMeter / k6

Send many requests concurrently and measure average latency, percentiles, throughput, and error rate.

![Debug the slowest trace on the slowest endpoint of a web service](https://images.openai.com/static-rsc-4/Jn6oUDOqX6BSngBFdHOag3U0Fu63bfnyThu9Ux5oSNZYNXjVlG7Cn35ZhVdcjIANjHs4FHiFdjLWfvLBLKWHKca7d2ssB5Xp9M4SaRz0llsCE2A8ire2cRKQi8z0o0n1sBJ76opHmwx6K_IJv3tbMEDznJQW3_26mVoqeWwGRfg?purpose=inline)

3. Datadog APM / New Relic APM

Monitor API performance in running environments and trace requests across Java services, databases, and downstream dependencies.

## 2. How to test response time in Postman

Example: `GET /employees/101`

1. Open Postman and send the API request.
    
2. Check the response time displayed with the status code.
    
3. Repeat the request several times.
    
4. Compare response time and status codes.
    
5. For concurrent traffic, run a performance test with virtual users.
    
    ![](https://www.google.com/s2/favicons?domain=https://learning.postman.com&sz=32)
    
    Postman Docs
    
    +1
    

For example:

HTTP Status

200 OK

Response time

## 180 ms

Illustrative result, not a live API test.

## 3. How do we test APM traces in Datadog?

Suppose your Spring Boot microservice has this flow:

API Gateway — 20 ms

Employee Service — 50 ms

Database SQL Query — 900 ms

### Total ≈ 970 ms

The exact total depends on how the timings are measured and whether they overlap.

Steps to investigate:

1. Install and configure the Datadog Java APM agent.
    
2. Enable instrumentation for your Spring Boot application and its supported libraries.
    
3. Send requests to the application.
    
4. Open Datadog → APM → Services and select your service.
    
5. Review request volume, errors, latency, and p95/p99.
    
6. Open a distributed trace for a slow request.
    
7. Inspect its spans to find the slow database query, downstream HTTP call, or application operation.
    

Distributed tracing records the journey of a request through instrumented services.

![](https://www.google.com/s2/favicons?domain=https://docs.newrelic.com&sz=32)

New Relic Documentation

+1

Useful official documentation:

- [Datadog APM](https://docs.datadoghq.com/tracing/?utm_source=chatgpt.com)
    
- [New Relic Java distributed tracing](https://docs.newrelic.com/docs/apm/agents/java-agent/configuration/distributed-tracing-java-agent/?utm_source=chatgpt.com)
    
- [Postman performance testing](https://learning.postman.com/docs/tests-and-scripts/test-apis/performance-testing/?utm_source=chatgpt.com)
    

## 4. Which tool should you use?

- Postman: Is this individual API responding quickly?
    
- JMeter or k6: Does the API remain fast with 100, 500, or 1,000 concurrent users?
    
- Datadog or New Relic: Why is the API slow in QA or production, and which component is responsible?
    

Interview-ready answer: “I use Postman for basic response-time checks, JMeter or k6 for load testing, and Datadog APM for production monitoring. I analyze p95/p99 latency and distributed traces to identify bottlenecks in application code, database queries, and downstream services.”