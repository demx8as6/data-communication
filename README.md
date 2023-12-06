# Data Communication
A place to discuss the need for several transport protocol and different encoding schemas in the context of a telecommunication network (RAN, Transport, Core, Cloud)

## Problem Statement
Looking for example  to the O-RAN Alliance OAM Specification there are 3 transport protocols to exhanchan data between a network-element/managed-element/network-function/device and its managing entity (NetworkManagementSystem, SMO, ...).
When extending to the view towards other O-RAN Alliance and 3 GPP defined interfaces it becomes even more complex. 

## Network Communication Protocols

| O-RAN/3GPP interface | Encoding   | Schema                  | Protocol               | Application Layer | Transport Layer | Network Layer | Data Link Layer | Reference                                               |
|----------------------|------------|-------------------------|------------------------|-------------------|-----------------|---------------|-----------------|---------------------------------------------------------|
| ./.                  | ./.        | ./.                     | HTTP                   | HTTP              | TCP             | IP            | Ethernet        | RFC 7230 (HTTP), RFC 791 (IPv4), RFC 894 (Ethernet)     |
| A1, O1               | json       | OpenAPISpec3 (or YANG?) | HTTPS                  | HTTP over TLS     | TLS over TCP    | IP            | Ethernet        | RFC 2818 (HTTPS), RFC 5246 (TLS), RFC 791 (IPv4)        |
| O1, OFHM             | xml (json) | YANG                    | NETCONF                | NETCONF           | SSH or TLS      | IP            | Ethernet        | RFC 6241 (NETCONF), RFC 4253 (SSH), RFC 791 (IPv4)      |
| ./. (R1?)            | RESTCONF   | json (or xml)           | RESTful API over HTTPS | HTTP over TLS     | TLS over TCP    | IP            | Ethernet        | RFC 8040 (RESTCONF), RFC 5246 (TLS), RFC 791 (IPv4)     |
| O1                   | xml        | 3GPP Spec               | FTPes                  | FTP over TLS      | TLS over TCP    | IP            | Ethernet        | RFC 4217 (FTP over TLS), RFC 5246 (TLS), RFC 791 (IPv4) |
| E2                   | ASN.1      | O-RAN Spec              | SCTP                   | SCTP              | SCTP            | IP            | Ethernet        | RFC 9260 (SCTP), RFC 791 (IPv4), RFC 894 (Ethernet)     |

## References

* [RFC 6241](https://www.rfc-editor.org/rfc/rfc6241.txt): [NETCONF](https://en.wikipedia.org/wiki/NETCONF)
* [RFC 9260](https://www.rfc-editor.org/rfc/rfc9260.txt): [SCTP](https://en.wikipedia.org/wiki/Stream_Control_Transmission_Protocol)
* [RFC 9293](https://www.rfc-editor.org/rfc/rfc9293.txt): [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)
* [RFC 768](https://www.rfc-editor.org/rfc/rfc9293.txt): [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol)
