stdin-stdout.conf

Simple config that takes stuff from stdin and dumps it back to stdout

stdin-stdout-ruby.conf

Same as 1, however, this time, instead of text, we show the JSON with some nice ruby colours

exec-stdout-ruby.conf

Execicute the "uptime" command every 5 seconds and output to stdout with Ruby JSON

exec-split.conf

Run the "ls -l /" command every 60 seconds, spliting the resulting lines into seperate events

exec-split-grok.conf (Broken -- see JIRA 1312)

Run the "ls -l /" command, split into multiple events, then GROK them 

tcp-stdout.conf

Open a TCP socket and wait for data. To send data to the socket use: 
nc localhost 8123

udp-stdout.conf

Open a UDP socket and wait for data. To send data to the socket use: 
nc -u localhost 8123

socket-stdout.conf

Open a UNIX socket and wait for data. To send data to the socket use: 
nc -U /tmp/lssock
