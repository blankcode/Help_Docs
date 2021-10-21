# Windows Error: "Connected, no internet"

"Connected, no internet": Can often mean a DNS issue is at fault. Most if not all Modern OSes reach out to a URL to see if "OY! This thing working??!!" If that query fails then "Connect, No Internet." This does NOT necessarily mean that the internet itself is down, or that your modem/router are to blame. _Also seen on Android and Linux._

### Tests:

On a command line: try reaching out to any IP. 8.8.8.8 on port 53 is an easy one.

Linux:

    $ dig +short google.com @8.8.8.8
    172.217.4.238

Windows CMD:

    nslookup google.com 8.8.8.8
    Server: dns.google
    Address: 8.8.8.8

    Non-authoritative answer:
    Name: google.com
    Addresses:  2607:f8b0:4009:800::200e
                172.217.4.110

_Your IP responses may/will vary_

If you are getting data back other than an Error then your internet is fine, but your DNS queries are having a problem.
