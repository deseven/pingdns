## pingdns
![pingdns](http://deseven.info/sys/pingdns.gif)  
A simple tool to "ping" (send a query and get an answer) the dns server.  
It's written to mimic the standard ping utility so it is really easy to understand the output.

## dependencies
sh  
grep  
dig

## compatibility
tested on CentOS 6 and OS X 10.10

## installation
Download the pingdns file, set the execution bit and make a symlink from /usr/bin/pingdns  
like that:  
```sh
curl https://raw.githubusercontent.com/deseven/pingdns/master/pingdns --output /opt/pingdns  
chmod +x /opt/pingdns  
ln -s /opt/pingdns /usr/bin/pingdns
```

## usage
dyndns dns [host]  
dns - dns server address (for example 4.2.2.2)  
host - hostname to use as a query, if empty it will be populated randomly  
Don't forget that query (and answer) validity is not important, what is important is the fact that we got an answer and how fast it happened.
