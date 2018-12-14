# Which one is more Secure? REST or SOAP

REST security is transport dependent while SOAP security is not.

REST inherits security measures from the underlying transport while SOAP defines its own via WS-Security.

When we talk about REST, over HTTP - all security measures applied HTTP are inherited and this is known as transport level security.

Transport level security, secures your message only while its on the wire - as soon as it leaves the wire, the message is no more secured.

But, with WS-Security, its message level security - even though the message leaves the transport channel it will be still protected. Also - with message level security you can partly encrypt the message [not the entire message, but only the parts you want] - but with transport level security you can't do it.

WS-Security has measures for authentication, integrity, confidentiality and non-repudiation while SSL doesn't support non repudiation [with 2-legged OAuth it does].

In performance-wise SSL is very much faster than WS-Security.

Thanks to https://stackoverflow.com/a/7218578/5703813
