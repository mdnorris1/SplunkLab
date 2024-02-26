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
<img src="assets/src ip.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

Using this ‘attacker IP’ that was uncovered, we can search for the IP address of the web server being targeted.

<br/> 
<img src="assets/dest ip.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

Next, we can transform the data into simple visualizations using the commands. 

After comparing these, let's look at some data that might be presenting possible attack scenarios.

<br/>
<img src="https://github.com/mdnorris1/WiresharkLab/blob/main/assets/css/packets3.png" height="80%" width="80%" alt="ifconfig command"/>
<br />

