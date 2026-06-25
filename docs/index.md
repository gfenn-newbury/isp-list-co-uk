# Welcome to ISP List UK

I created this website to list ISPs in the UK and their features. I was fed up going around multiple sources to try and find basic things, like whether an ISP uses CG-NAT, whether they use IPv6 and if so, what prefix length do they give out, whether you can use your own equipment, etc.

This website lists ISPs in the UK, and their features, in a hopefully simple way to compare them.


## What is CG-NAT and why should I care?

The short answer: 

CG-NAT is a way to share a single public IP across an entire neighbourhood, rather than each household having one (regular NAT) or even each device having a public IP address. Like NAT, it breaks the principle of end-to-end connections that the internet was built on. This has implications for both businesses and consumers in applications such as IP telephony, gaming, and connection monitoring and management. It can even lead to issues with accountability if someone does something illegal on the internet, as that IP address could now lead to an entire neighbourhood rather than an individual household or even specific device. 

In an ideal world, every device connecting to the internet should have its own unique IP. **This is solved with IPv6, but not all ISPs offer this despite it being standardised over 30 years ago.** This is largely down to laziness rather than inability.

The longer answer is...

### What is NAT and why was it introduced?

First of all, let's talk about NAT, and why it was introduced. In the beginning of the IP-based internet, public IP addresses were the only type of IP addresses. Your device would have an IP address (eg, `1.1.1.1`), and somebody elses device would have a different IP address (eg, `1.1.1.2`). These two devices, using these IP addresses, could then communicate directly with each other. Each device on the internet had to have a unique IP address in order to communicate.

However, there are only ~4 billion IPv4 (the type of IP address denoted by `w.x.y.z`) addresses available (`0.0.0.0` - `255.255.255.255`). It was known from the early days of the internet that this wouldn't be enough as computers became ubiquitous, and once we ran out, new devices wouldn't be able to be assigned one. 

While a long term solution was developed (which became IPv6), someone came up with an idea to allow IPv4 to live on a bit longer. Take a group of IP addresses, and mark them as private addressess. These addresses would be used in a local network (think within a household), but couldn't be used on the wider internet. Then, give this local network gateway device with a single "public" address. When a device on the local network needed to talk to the internet, it would communicate with this gateway which would then act as a middleman between the device and the internet. And voila, **N**etwork **A**ddress **T**ranslation, where one address gets translated to another to communicate across the internet, was born.

This allowed the internet to get the widespread adoption we see today. However, it only delayed the issue of there not being enough IPv4 addresses rather than solve it.

### What is CG-NAT compared to NAT?

CG-NAT is a type of nested NAT. Where when using regular NAT, a public IP address might be assigned to a single household, in CG-NAT, a public IP address is shared amongst multiple households or entire neighbourhoods. This can create network issues for applications, such as those that rely on only having one connection from a single public IP at a time, or those which monitor and ban IP addresses which seem nefarious. In the example of IP address bans, one person in a neighbourhood which is sharing an IP address could do something nefarious and get the IP banned, meaning everyone else in the neighbourhood wouldn't then be able to use that service.

## What is IPv6 and why should I care?

IPv6 is the new (well, 30 years old, but newer than IPv4) way of addressing devices on the internet. There are so many addresses in IPv6 that individuals could have thousands of devices, and they would still have unique IP addresses. IPv6 has no need for NAT, and restores the end-to-end connection principle that the internet was founded on.