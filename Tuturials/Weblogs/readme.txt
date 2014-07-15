3-weblog-stdout.conf

We start playing with weblogs - dump the JSON to stdout

4-weblog-filter-stdout.conf

We take the data from 3, and pass it thought a GROK filter to parse out the web logs

5-weblog-filter-es.conf

Here we take 3 and dump it into an ElasticSearch cluster on localhost using HTTP connector. Note that if you type into stdin you'll get an event with _grokparsefailure tag

6-weblogs-tags.conf

Adding tags to 3 and dump it to stdout

7-weblogs-tags-conditional.conf

Remove any _grokparsefailure using a conditional in tags, and remove them. In this case, you'll see events from Weblogs, however typing into stdin will yeild nothing returned.

8-weblogs-date.conf

Parse the date field from 4 and modify the internal timestamp

9-weblogs-date-parsedate.conf

Same as 8, however we keep the date/time the event was parsed

10-weblogs-date-age.conf

Calculate the age of the event from Generation (from log) to parse

11-weblogs-anonymize-A.conf

Anonymize the clientip field using the default SHA1 hash

12-weblogs-anonymize-B.conf

Anonymize the clientip field using IPV4_NETWORK option - note that the first 2 octets are kept.

13-weblogs-metric.conf

Reads the weblogs, and displays metrics on the response codes. 

14-weblogs-useragent.conf

Reads the weblogs and gathers information about the user agent
