# tcptools

## Using "ping" (3 pts)
```ping``` three popular websites (for 5 or so packets each)

- Ping www.amazon.com three times
- Ping www.google.com  three times
- Ping www.microsoft.com three times

### Answer the following questions:

- What were the min/avg/max/stddev statistics for each?
- Was there any packet loss on any of the pings?
- Did the IP address change for a given website between pings?

**www.amazon.com**: yes

**www.google.com**: no

**www.microsoft.com**: no

1st ping:
| Questions                                                    |  www.amazon.com               | www.google.com                 | www.microsoft.com              |
| ------------------------------------------------------------ | ----------------------------- | ------------------------------ | ------------------------------ |
| What were the min/avg/max/stddev statistics for each?        | 14.467/17.006/18.519/1.451 ms | 18.301/20.641/24.016/2.133 ms  | 16.852/18.090/20.386/1.219 ms  |
| Was there any packet loss on any of the pings?               | 0.0% - No                     | 0.0% - No                      | 0.0% - No                      |

2nd ping:
| Questions                                                    |  amazon.com                   | google.com                     | microsoft.com                  |
| ------------------------------------------------------------ | ----------------------------- | ------------------------------ | ------------------------------ |
| What were the min/avg/max/stddev statistics for each?        | 15.997/17.183/19.342/1.137 ms | 14.523/16.262/18.595/1.335 ms  | 14.488/16.461/17.954/1.325 ms  |
| Was there any packet loss on any of the pings?               | 0.0% - No                     | 0.0% - No                      | 0.0% - No                      |

3rd ping:
| Questions                                                    |  amazon.com                   | google.com                     | microsoft.com                  |
| ------------------------------------------------------------ | ----------------------------- | ------------------------------ | ------------------------------ |
| What were the min/avg/max/stddev statistics for each?        | 15.477/18.629/25.675/3.619 ms | 15.309/17.300/19.651/1.501 ms  | 12.875/19.589/28.159/4.968 ms  |
| Was there any packet loss on any of the pings?               | 0.0% - No                     | 0.0% - No                      | 0.0% - No                      |


## Using "tracert" (2 pts)
Use ```tracert``` (or ```traceroute```, depending on your OS) on the following sites:

- www.amazon.com
- www.google.com
- www.microsoft.com

### Answer the following questions:

| Question                                       | www.amazon.com | www.google.com|www.microsoft.com|
| ---------------------------------------------- | -------------- | ------------- | --------------- |
| What was the target server's IP address?       | 23.45.229.96   | 142.251.33.68 | 23.216.81.152   |
| How many hops were needed to reach the target? | 10             | 11            | 14              |

- Can you identify your ISP from the intermediate server DNS names?
Yes - Comcast
- Identify the "class" of IP address for each major step in the trip
- 
**www.amazon.com**: Apart from my IP address (Class C) and the first hop (Class B), everything else is Class A

**www.google.com**: My IP address is Class C and the first hop is Class B. As it hops around, it stays mostly as a Class A IP address. Once its in the google network, it becomes a Class B IP address.

**www.microsoft**: Apart from my IP address (Class C) and the first hop (Class B), everything else is Class A

## Extra credit: Using packet-capture tools (2 pts)
Capture the DHCP traffic for your laptop
- Filter out any extraneous traffic so we see only the DHCP traffic
- Submit a screenshot of the DORA process and the lease time offered by the DHCP server.

<img width="1512" alt="Screenshot 2023-04-04 at 12 42 39 PM" src="https://user-images.githubusercontent.com/62910852/229902554-4e6712d5-819a-48bc-b016-2f4535289068.png">

## Extra credit: Insecure web server (2 pts)
Download/install Wireshark
- Navigate to http://150.230.36.255/
- Submit the login form with any email and password while capturing packets with Wireshark.
- Filter out any extraneous traffic so we see only the traffic to the server
- Take a screen shot of Wireshark showing the payload you sent to the server
- Store the screen shot in the Github repo
<img width="955" alt="Screenshot 2023-04-03 at 10 37 37 PM" src="https://user-images.githubusercontent.com/62910852/229697649-43c76e11-caff-408e-98fb-b0f57caa659c.png">

