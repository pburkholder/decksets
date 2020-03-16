Theme: Next, 1
text: Libre Franklin, #53585F
text-strong: Libre Franklin, #EE783F
text-emphasis: Libre Franklin Italic
header: Libre Franklin, #53585F
header-strong: Roboto Strong,#EE783F
header-emphasis: Reklame Script, #53585F  
code: Fira Code Medium, #EE783F, #8B3D90, #2E59A2, #DF393F, #1EA8D9
background-color: #FFFFFF  
slidenumbers: true
footer: ![inline 8%](https://www.cloudfoundry.org/wp-content/uploads/2017/10/cloud-gov.png) 
build-lists: true

# TLS is 2 things:

1. - 🔐 - Encrypted transport
2. - ✅ - Service entity validation

---

# 🔐 - Encrypted transport

The encryption is agreed upon between the client and services. Most clients don't agree to use weak encryption. All the services we run use strong well-supported encryption. It's not in the picture when we talk about Let's Encrypt vs., say, DigiCert

---

# ✅ - Service entity validation

How do you know, when browsing to `example.gov` that the page is actually coming from `example.gov`, and not `evil.ru`?

From the server certificate with a signature from a Certificate Authority (CA)

---

# The conversation

- When the client connects with the server, it says "ClientHello" - I accept these ciphers, lets' talk.
- The server replies, "Cool, here's my Server Certificate proving I'm example.gov"

The client now validates the server's certificate

---

# The validation

The server certification is signed by a "Certificate Authority"

The client has a list, e.g. Firefox: about:preferences#privacy

It checks if the Server Certificate has a valid signature that can be traced back to the Certificate Authority.

---

# Key point as server operator:

**From a server operator's perspective, any CA is identical to any others: the clients will treat them the same. Use the cheapest and easiest one.**

I have felt this way since 2002, and nothing since then has change my perpspective. (https://www.sans.org/reading-room/whitepapers/threats/paper/480)

---

# Key point as a desktop system manager:

From a client (desktop) operator's prespective, I may want to restrict CAs, as .mil does.

---

https://dl.dod.cyber.mil/wp-content/uploads/pki-pke/zip/unclass-dod_approved_external_pkis_master_document_v6-3_20180305-1.pdf

 DoD Approved External PKI Certificate Trust Chains - Version 7.3
 https://public.cyber.mil/pki-pke/interoperability/


--- 

Commercial CAs have had their own issues:

* https://www.pcworld.com/article/3157406/godaddy-revokes-nearly-9-000-ssl-certificates-issued-without-proper-validation.html
* https://www.digicert.com/replace-your-symantec-ssl-tls-certificates/

---

Who is Let's Encrypt?

- Funding
- Board of Directors
- Why they exist

--- 

Growth of TLS is good, EVs are now deprecated.

---

All the downsides of Let's Encrypt are features, not bugs 

---

What happened with this issue and why the revocations?

Remember LE has now issued 1Bn certs...

---

The protection is DNS is not relevant. Even if you don't use LE, if you don't control your DNS, then someone else could.

DNSSEC is a different issue.



