# Splunk

My first project here is focussing on Searching terms useful for Splunk.

First, query the data for key pieces of information using the techniques/commands - commands indicate certain actions that you want to perform on the results of a given search. This can include filtering, sorting, counting, renaming, or generating commands as well as others.

So, for example, you can use the command TOP to show the most common of field values, for example the destination port (see image below) in a dataset.

We looked at the least common value by using the command RARE.

<br/>
<img src="https://github.com/mdnorris1/SplunkLab/blob/main/assets/1%20top.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

We can perform a search using the stats command to count the number of events present by a particular field. Notice below how it auto-suggests possible commands when you start typing.

<br/>
<img src="assets/stats .png" height="80%" width="80%" alt="ifconfig command"/>
<br />

Next, we could carry out a search on a website domain name and then on the next line, use the 'top' command to determine the possible IP address of an attacker scanning this domain name for vulnerabilities.

<br/>
<assets/src ip.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

Next, we can transform the data into simple visualizations using the commands. 

After comparing these, let's look at some data that might be presenting possible attack scenarios.

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/packets3.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

This gives us a breakdown of who was chatting with what system the most.  Click it again and it will sort the opposite direction and show you the least:

Really want to know what those systems were saying to each other?  Right click on a conversation and select Apply as Filter > Selected > A<->B

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/filter4.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

You should see the main Wireshark screen change

Then, close the Conversations window.

Notice the following in the filter bar

`ip.addr==68.183.138.51 && ip.addr==192.168.99.52`

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/filterbar5.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

This is saying:

"IP address equals 68.183.138.51 And IP address equals 192.168.99.52"

If a packet meets both of those critiera it is displayed.

Now, right-click on any of the packets and select Follow > TCP Stream:

This is showing the request (in red) and the response (in blue) between our two systems:

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/request6.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

There is a lot of encoded PowerShell here.

I then got to try some basic filters in the filter bar, so after filtering on IP addresses, I was now filtering on protocols.

using the filter: llmnr.

Then hit enter.

Notice that when you type llmnr and hit enter, Wireshark shows you all packets that are that protocol

Now try ipv6 and hit enter:

This allows you to very quickly drill in on any specific protocols you are reviewing in a packet capture.

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/ipv67.png" height="80%" width="80%" alt="ifconfig command"/>
<br />
