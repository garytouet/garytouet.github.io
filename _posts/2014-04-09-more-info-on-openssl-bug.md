---
id: 970
title: More info on the OpenSSL bug
date: 2014-04-09T09:23:10+00:00
author: Gary
layout: post
guid: http://garytouet.com/?p=970
permalink: /2014/04/more-info-on-openssl-bug/
link:
  - http://www.vox.com/2014/4/8/5593654/heartbleed-explainer-big-new-web-security-flaw-compromise-privacy
categories:
  - Links
  - Technology
---

Timothy B. Lee for Vox:
<blockquote>Here's how it works: the SSL standard includes a heartbeat option, which allows a computer at one end of an SSL connection to send a short message to verify that the other computer is still online and get a response back. Researchers found that it's possible to send a cleverly formed, malicious heartbeat message that tricks the computer at the other end into divulging secret information. Specifically, a vulnerable computer can be tricked into transmitting the contents of the server's memory, known as RAM.</blockquote>

Useful to note that patching the servers is not enough, companies need to reissue all the private keys in order to solve the problem. An attacker could have gain access to those and still use them to steal information once the servers are patched.
