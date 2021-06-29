# Jmeter

my custom jmeter  

first click `startAgent.bat` in directory : `C:\jmeter\ServerAgent`  
then click `jmeter.bat` in directory : `C:\jmeter\bin`

# Run Not GUI mode

```
jmeter -n -t API.jmx -l result.csv
```

# Add to environment

add `C:\jmeter\bin` to `Path`

# Info

## Summary Report
The summary report creates a table row for each differently named request in your test. This is similar to the Aggregate Report , except that it uses less memory.  

-   `Label` : The label of the sample. If "Include group name in label?" is selected, then the name of the thread group is added as a prefix. This allows identical labels from different thread groups to be collated separately if required.
-   `Samples` : The number of samples with the same label
-   `Average` : The average elapsed time of a set of results
-   `Min` : The lowest elapsed time for the samples with the same label
-   `Max` : The longest elapsed time for the samples with the same label
-   `Std. Dev.` : the Standard Deviation of the sample elapsed time
-   `Error %` : Percent of requests with errors
-   `Throughput`:- the Throughput is measured in requests per second/minute/hour. The time unit is chosen so that the displayed rate is at least 1.0. When the throughput is saved to a CSV file, it is expressed in requests/second, i.e. 30.0 requests/minute is saved as 0.5.
-   `Received KB/sec` : The throughput measured in Kilobytes per second
-   `Sent KB/sec` : The throughput measured in Kilobytes per second
-   `Avg. Bytes` : average size of the sample response in bytes.

## Aggregate Report
The aggregate report creates a table row for each differently named request in your test. For each request, it totals the response information and provides request count, min, max, average, error rate, approximate throughput (request/second) and Kilobytes per second throughput. Once the test is done, the throughput is the actual through for the duration of the entire test.

-   `Label` : The label of the sample. If "Include group name in label?" is selected, then the name of the thread group is added as a prefix. This allows identical labels from different thread groups to be collated separately if required.
-   `Samples` : The number of samples with the same label
-   `Average` : The average time of a set of results
-   `Min` : The median is the time in the middle of a set of results. 50 % of the samples took no more than this time; the remainder took at least as long.
-   `90% Line` : 90 % of the samples took no more than this time. The remaining samples took at least as long as this. (90th percentile)
-   `95% Line` : 95 % of the samples took no more than this time. The remaining samples took at least as long as this. (95th percentile)
-   `99% Line` : 99 % of the samples took no more than this time. The remaining samples took at least as long as this. (99th percentile)
-   `Min` : The shortest time for the samples with the same label
-   `Max` : The longest time for the samples with the same label
-   `Error %` : Percent of requests with errors
-   `Throughput` : the Throughput is measured in requests per second/minute/hour. The time unit is chosen so that the displayed rate is at least 1.0. When the throughput is saved to a CSV file, it is expressed in requests/second, i.e. 30.0 requests/minute is saved as 0.5.
-   `Received KB/sec` : The throughput measured in received Kilobytes per second
-   `Sent KB/sec` : The throughput measured in sent Kilobytes per second

## View Results in Table
he View Results Tree shows a tree of all sample responses, allowing you to view the response for any sample. In addition to showing the response, you can see the time it took to get this response, and some response codes. Note that the Request panel only shows the headers added by JMeter. It does not show any headers (such as Host) that may be added by the HTTP protocol implementation.

-   `Latency` : The number of milliseconds that elapsed between when JMeter sent the request and when an initial response was received
-   `Sample Time` : The number of milliseconds that the server took to fully serve the request (response + latency)


# Note
I change `sigar-amd64-winnt.dll` in `C:\jmeter\ServerAgent\lib` because of bug on Sigar library. [More Info](https://github.com/hyperic/sigar/issues/141)
