# ISP Overview

This list intends to give an overview of what each ISP offers as a **default**. Some of them may offer static IPv4 addresses, bigger IPv6 ranges, or other goodies at an extra cost.

Additionally, there are several "types" of IPv4 address. These are:

- Static - A public, non-changing IP address, that's assigned to you for as long as your service is live
- Sticky - A public, rarely changing IP address, which normally changes if your router reboots or after a certain amount of time (usually weeks)
- CG-NAT - The type of IP address we want to avoid

!!! info
    This table is a work in progress. If you know the details of something marked unknown, please raise a pull request


| ISP Name           | IPv4                                  | IPv6                                                           | Use own router?                   | Providers         | Parent Company |
| ------------------ | ------------------------------------- | -------------------------------------------------------------- | --------------------------------- | ----------------- | -------------- |
| Andrews and Arnold | Static                                | Yes, /48                                                       | Yes                               | Openreach         | N/A            |
| Cuckoo             | <span style="color:red">CG-NAT</span> | Yes, /48                                                       | Unknown                           | APFN              | Fern Trading   |
| IDNet              | Static                                | Yes, /48                                                       | Yes                               | Openreach, Trooli | N/A            |
| Virgin Media       | Sticky                                | <span style="color:red">No</span><a href="#footnote-1">^1^</a> | Yes^2^                            | Themselves        | Liberty Global |
| EE                 | Unknown                               | Unknown                                                        | Unknown                           | Openreach         | BT             |
| PlusNet            | Unknown                               | Unknown                                                        | Unknown                           | Openreach         | BT             |
| Trooli             | <span style="color:red">CG-NAT</span> | Unknown                                                        | <span style="color:red">No</span> | Themselves        | Themselves     |
| Toob               | Unknown                               | Yes, /48                                                       | Unknown                           | Themselves        | Themselves     |

<span id="footnote-1"> ^1. This has been an [on-going battle for more than a decade](https://www.havevirginmediaenabledipv6yet.co.uk/). </span></br>
<span id="footnote-2"> ^2. Requires using the Virgin Media router in "modem mode". </span>