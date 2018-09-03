---
layout:     post 
title:      "Thoughts on Applying \"Security in Depth\" to Microservices"
date:       2017-10-08
author:     "Brian Avery"
URL: "/2017/10/08/thoughts-on-applying-security-in-depth-to-microservices"
image:      "https://img.zhaohuabing.com/post-bg-2015.jpg"
---

The world of microservices divides programs up into several chunks. With this division comes several questions one of which is the security vs load. If each of your services verify a user token against an authentication system, then that creates a lot of load. If you verify at the perimeter of your network, then you've verified that the user is valid at the the perimeter of your network, and if no other services other than the services that are verifying authentication are exposed, you're safe right? What happens if your network is compromised though?

<strong>Logs
</strong>If your network is compromised, then your logs are most likely compromised as well. Be careful of what information you store in your logs.

<strong>Network Traffic</strong>
If your network is compromised, be careful of HTTP/HTTPS traffic, because the attacker can probably sniff that traffic and observe content traveling between services. If you use certificates between services then you're able to encrypt, but you can't generate valid certificates against IP addresses, and with host names you need to create a certificate for each deploy of the service. Running with unverified certificates is little better than not encrypting at all because you are not verifying the source of the packet.

<strong>Service Access to Other Services
</strong>Can a stray service access any/all content from other services? If a compromised service makes requests to other services in the network, can it access any information that it wants? Perhaps a system similar to oauth could be used in which different APIs have scopes attached to them and the scopes would be verified against a certificate created by that service at launch. This would make it easier to audit the actions that a service is taking as well as limit the service to only performing specific actions. Efforts would need to be taken to reduce the load that requests are making on the network. If the certificate is created at service launch, then that would mean that the token for the originator would only have to be created once, but that the token would have to be verified each time a request is made. This information could probably be stored in a system such as Redis.

<strong>Service Configuration
</strong>Microservices are cattle. They can be killed off at a moments notice and a new one will take its place in a few milliseconds. In a production environment, there will usually be more than one instance of a service running and these other instances can pick up the load in the mean time. This is great, but it means that there is no human involved and the service must be able to pick up its settings automatically. Services such as Zookeeper, ETCD, and configuration files help with this, but these settings are still stored on the network. Be careful of how this configuration is handled, especially for data such as passwords and other credentials for the service.

<strong>Database Access
</strong>If an attacker gains access to your network, can they gain access to the database? If they gain access to the database, can they gain access to information such as usernames/passwords/social security numbers/other confidential information? Be careful of encrypting the confidential data in your product, both in flight and at rest.

Each of these has a trade off. Speed vs security. How big is the risk that someone might gain access to this information? How much damage will it cause if this access is gained. The higher the risk, the more consideration should be put into the confidentiality of your data. Microservices are cheap. If one service is under load, scale up more to handle the traffic that that service cannot handle.