---
layout:     post 
title:      "MIT IoT Security Conference"
date:       2016-03-10
author:     "Brian Avery"
URL: "/2017/03/10/mit-iot-sec-conference"
image:      "https://img.zhaohuabing.com/post-bg-2015.jpg"
---



<div class="gmail_msg">During the weekend of March 5-6, the <span class="lG">MIT</span> Media Lab hosted a conference focused on the Security of the Internet of Things. <span class="gmail_msg">With the internet of things, we have many new devices, such as cars, baby monitors, thermostats, electrical outlets, and a </span><span class="gmail_msg">host of other devices coming onto the internet. As more and more of these devices come online, security is becoming and will </span><span class="gmail_msg">continue to become an even greater concern. This was the focus of the event.</span></div>
<div class="gmail_msg"></div>
<div class="gmail_msg">The event included both a foundation of the current and future states of IoT security and hands on application with real-world <span class="gmail_msg">devices.  Bruce Schneier, was recently back from a trip to the RSA conference and made an appearance to give a similar talk at </span><span class="gmail_msg">the <span class="lG">MIT</span> conference. In this talk, he presented a couple of ideas. First, IoT is just starting to take off. The technology industry </span><span class="gmail_msg">is rapidly working to bring more and more devices on the internet. These devices are produced first and foremost with a concern for</span><span class="gmail_msg">getting the device to market faster than the competitors, and security as an afterthought. As the industry matures, security will</span></div>
<div class="gmail_msg">take more and more of a spotlight. New government organizations will be created to manage the security of devices, regulations on <span class="gmail_msg">software will be created, further education, and other measures will be applied. Even with all of this, however, Schneier did not believe </span><span class="gmail_msg">that we will be able to truly secure the industry. Eventually there will be a point where we decide that not every device needs to be on the internet </span><span class="gmail_msg">and the number of devices will begin to shrink.</span></div>
<div class="gmail_msg"></div>
<div class="gmail_msg">Several speakers discussed issues with the ways that companies use open source libraries. As a result of all of these devices being rushed to market, manufacturers of devices often release firmware releases without ever updating the open source libraries that are a part of their codebase. As time goes on, more and more vulnerabilities are discovered in these libraries, <span class="gmail_msg">and even though the code written by the company itself gets patched, the products have increasingly more vulnerabilities until the libraries </span><span class="gmail_msg">are updated. These speakers made sure to emphasize that even though a library was included in a project did not mean that the area of code with the vulnerability </span><span class="gmail_msg">was accessed, and therefore not all were vectors for attack.</span></div>
<div class="gmail_msg"></div>
<div class="gmail_msg">The talks occupied much of the morning, but after lunch, both days included hands on activities. <span class="lG">MIT</span>supplied several devices including thermostats, electrical outlets,<span class="gmail_msg">drones, and light bulbs. The first hands on activity was presented by Synopsys. Synopsys provided a copy of their tool Protecode-SE for attendees to use with these devices</span><span class="gmail_msg">i n order to look at the firmware and see what vulnerabilities existed. Attendees could then attempt to break into these devices. Many vulnerabilities were found and some </span><span class="gmail_msg">groups even succeeded in breaking into their devices.</span></div>
<div class="gmail_msg"></div>
<div class="gmail_msg">On the second day, there were two hands on activities. The first was presented by Defensics. Defensics provided a fuzzer that they had produced. A fuzzer is a tool that <span class="gmail_msg">takes a valid input for a device whether it be file, HTTP, SNMP, SMTP, or some other protocol and tries different permutations on the input to see how the device reacts.</span><span class="gmail_msg">If a device handles the input incorrectly, then it may be a possible attack vector. Groups were able to apply this tool to their devices to see what the results were. </span><span class="gmail_msg">One group had a lot of luck with the thermostat that they were supplied. It was suggested that all software companies include a fuzzer in the testing measures for their products.</span></div>
<div class="gmail_msg"></div>
<div class="gmail_msg">To wrap up the event, a startup sponsoring the event called DoJo labs supplied a device that they were creating to bring security to IoT Devices. This device that monitors traffic patterns on a home network to see when a device is acting improperly and notify the user. Each device is authorized on a  network and with what permissions it should have (all network, no network, specific resources). Traffic patterns for devices are monitored globally. If a device all of a sudden starts sending traffic to a new destination, increased traffic, new protocols, or otherwise odd behavior, the device flags this as a possible threat and notifies the user if it’s not registered as a threat, or handles it itself if it is registered. This looks like a very interesting device that has the potential to take off as IoT security becomes more of a concern.</div>
<div class="gmail_msg"></div>
<div class="gmail_msg">As a software engineer, I found this event to be a lot of fun and would definitely encourage others in the industry to attend as well. I found the event to provide a solid foundation in the state of security, an understating of how to improve the security in software that I write, and fun hands on activities. I believe that this event has served to help me understand the issues with security and how to improve it in my own products. I look forward to the next event.</div>