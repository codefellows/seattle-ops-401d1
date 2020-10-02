# Ops Challenge - Web Application Fingerprinting Part 3 of 3 

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python

import urllib
import urllib2

location = "http://test_target.site/login.aspx"
values = {"username":"'","password":"password","btnSubmit":"Login"}
data = urllib.urlencode(values)
req = urllib2.Request(location,data)
response = urllib2.urlopen(req)
page_data = response.read()

print page_data

```
"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


