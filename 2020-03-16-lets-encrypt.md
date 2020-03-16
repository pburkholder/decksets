TLs is 2 things

1 - Lock - End-to-end encryption
2 - CheckMark - Service entity validation

--

1 - The lock is agreed upon between the client and services. Most clients don't agree to use weak encryption. All the services we run use strong well-supported encryption. 
  It's not in the picture when we talk about Let's Encrypt vs., say, DigiCert
2 - The checkmark - how do you know, when browing to `example.gov` that the page is actually coming from `example.gov`, and not `evil.ru`?

--

The conversation:

- When the client connects with the server, it says "ClientHello" - I accept these ciphers, lets' talk.
- The server replies, "Cool, here's my Server Certificate proving I'm example.gov"

The client now validates the server's certificate

---

The server certification is signed by a "Certificate Authority"

The client has a list, e.g. Firefox: about:preferences#privacy

It checks if the Server Certificate has a valid signature that can be traced back to the Certificate Authority.

--

# Key point: From a server operator's perspective, any CA is identical to any others: the clients will treat them the same. Use the cheapest and easiest one.

I have felt this way since 2002, and nothing since then has change my perpspective. (https://www.sans.org/reading-room/whitepapers/threats/paper/480)

# Key point: From a client (desktop) operator's prespective, I may want to restrict CAs:

https://dl.dod.cyber.mil/wp-content/uploads/pki-pke/zip/unclass-dod_approved_external_pkis_master_document_v6-3_20180305-1.pdf

 DoD Approved External PKI Certificate Trust Chains - Version 7.3
 https://public.cyber.mil/pki-pke/interoperability/


--- 

CA's screw up too:

* https://www.pcworld.com/article/3157406/godaddy-revokes-nearly-9-000-ssl-certificates-issued-without-proper-validation.html
* Symantec has been a dumpster fire


