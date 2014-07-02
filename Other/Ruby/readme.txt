convert-to-ms.conf

Two possible numbers, one in ms on in seconds. Wanted to convert to ms.

delete_nested_fields.conf

Delete a nested field inside an event. There's no clear way to do this using
just Logstash, but it's easy to use the 'ruby' filter and modify the event
information from there.
