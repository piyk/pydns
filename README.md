# pydns
* The codes includes dns utilities wrappers for dnslib


### dnsserver.py provides a simple of custom DNS server and example of domain in SOA/NS records.
```
Starting nameserver...
UDP server loop running in thread: Thread-1
TCP server loop running in thread: Thread-2

UDP request 2020-01-13 07:12:18.296781 (127.0.0.1 54251):
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 6699
;; flags: rd; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 0
;; QUESTION SECTION:
;udru.ac.th.                   IN      A
---- qname:  udru.ac.th.
---- D:  udru.ac.th.
---- Reply:
 ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 6699
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 0
;; QUESTION SECTION:
;udru.ac.th.                   IN      A
;; ANSWER SECTION:
udru.ac.th.            300     IN      NS      10.10.10.11
```

### proxy.py is a part of the dnslib, providing DNS proxy server.
```
Starting Proxy Resolver (*:53 -> 8.8.8.8:53) [UDP]
Request: [127.0.0.1:64360] (udp) / 'google.com.' (A)
Reply: [127.0.0.1:64360] (udp) / 'google.com.' (A) / RRs: A
Request: [127.0.0.1:64363] (udp) / 'facebook.com.' (A)
Reply: [127.0.0.1:64363] (udp) / 'facebook.com.' (A) / RRs: A
Request: [127.0.0.1:52493] (udp) / 'udru.ac.th.' (A)
Reply: [127.0.0.1:52493] (udp) / 'udru.ac.th.' (A) / NXDOMAIN
Request: [127.0.0.1:52495] (udp) / 'udru.ac.th.' (A)
Reply: [127.0.0.1:52495] (udp) / 'udru.ac.th.' (A) / SERVFAIL
Request: [127.0.0.1:60529] (udp) / 'sci.udru.ac.th.' (A)
Reply: [127.0.0.1:60529] (udp) / 'sci.udru.ac.th.' (A) / SERVFAIL
Request: [127.0.0.1:60551] (udp) / 'sci.udru.ac.th.' (A)
Reply: [127.0.0.1:60551] (udp) / 'sci.udru.ac.th.' (A) / NXDOMAIN
Request: [127.0.0.1:60558] (udp) / 'kku.ac.th.' (A)
Reply: [127.0.0.1:60558] (udp) / 'kku.ac.th.' (A) / RRs: A
Request: [127.0.0.1:60561] (udp) / 'msu.ac.th.' (A)
Reply: [127.0.0.1:60561] (udp) / 'msu.ac.th.' (A) / RRs: A
```
