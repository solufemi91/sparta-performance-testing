# sparta-performance-testing

In order to run the tests in these files, you need to have JMeter installed. To do this, go to http://jmeter.apache.org/download_jmeter.cgi.

How to write test plan in Jmeter

First create a threadgroup by right clicking on the test plan - Add - Thread - Threadgroup.

In the threadgroup:

right click- add-config element- HTTP Request Default

right click- add-config element- HTTP Header Manager

right click- add-sample- HTTP Request

right click- add-listerners-view results tree

right click- add-sampler- debug sampler

right click- add-listeners- summary report

Inside HTTP request:

right click- add - assertion- response assertion

right click- add - post processor - JSON Extractor

Use of each page

In the Test Plan you declare your variables.

The thread group is used to put the conditions for your tests, e.g number of users: 100, Ramp up Period: 1 second, Forever: 1 - This would be a spike test.

In HTTP request defaults you put http and source of the website url.

In HTTP header manager you put the type it is for example: name - content-type, value - Application/Json

In HTTP Request you input the path of the part of the website you want to test and whether it is a post or get request etc.

The JSON Extractor is used to get back specific data in the JSON. Make sure to put No_Default in default values so no empy values will be returned.

The response assertion is used to check a specific item is in the data.

The results tree is where you see the results of the data.
