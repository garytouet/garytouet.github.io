---
id: 968
title: Critical crypto bug found in OpenSSL
date: 2014-04-09T09:10:55+00:00
author: Gary
layout: post
guid: http://garytouet.com/?p=968
permalink: /2014/04/critical-crypto-bug-found-in-openssl/
link:
  - http://arstechnica.com/security/2014/04/critical-crypto-bug-in-openssl-opens-two-thirds-of-the-web-to-eavesdropping/
categories:
  - Links
  - Technology
---

ArsTechnica:
<blockquote>Researchers have discovered an extremely critical defect in the cryptographic software library an estimated two-thirds of Web servers use to identify themselves to end users and prevent the eavesdropping of passwords, banking credentials, and other sensitive data.

[…]

The researchers, who work at Google and software security firm Codenomicon, said even after vulnerable websites install the OpenSSL patch, they may still remain vulnerable to attacks. The risk stems from the possibility that attackers already exploited the vulnerability to recover the private key of the digital certificate, passwords used to administer the sites, or authentication cookies and similar credentials used to validate users to restricted parts of a website. Fully recovering from the two-year-long vulnerability may also require revoking any exposed keys, reissuing new keys, and invalidating all session keys and session cookies.
</blockquote>

Fuck.
