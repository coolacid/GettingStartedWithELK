This sample shows how to parse the common Rails request log format,
however, it can easily be adapted for any log format that uses a common
"header", followed by multiple arbitrary message formats.

The most important part of this pattern, especially if you're looking to
apply it to other log types, is the matching of the header information in
a dedicated grok filter, and then using one or more separate filters to parse
the various "sub-message" formats.
