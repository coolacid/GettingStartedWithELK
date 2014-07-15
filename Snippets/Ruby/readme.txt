convert-to-ms.conf

Two possible numbers, one in ms on in seconds. Wanted to convert to ms.

delete_nested_fields.conf

Delete a nested field inside an event. This is an alternative to doing it via
the Logstash way using:
    
    ` mutate { remove_fields => ... }`

It's easy to use the 'ruby' filter and modify the event information from there.
