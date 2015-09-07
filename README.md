## pingdns
![pingdns](http://deseven.info/sys/pingdns.gif)  
A simple tool to "ping" (send a query and get an answer) the dns server.  
It's written to mimic the standard ping utility so it is really easy to understand the output.

## dependencies
bash  
grep  
dig

## compatibility
tested on CentOS 6/7, Debian 7 and OS X 10.10

## installation
Download the pingdns file, set the execution bit and make a symlink from /usr/bin/pingdns  
like that:  
```sh
curl https://raw.githubusercontent.com/deseven/pingdns/master/pingdns --output /opt/pingdns  
chmod +x /opt/pingdns  
ln -s /opt/pingdns /usr/bin/pingdns
```

## usage
**pingdns [-hctqrs] dns**  
**dns** - dns server address  
**-h** to show the help  
**-c count** to stop after sending 'count' requests  
**-t sec** to set the query timeout to 'sec' seconds  
**-q query** to force sending the defined 'query'  
**-r** to generate random queries  
**-s** to be silent and print only results  
By default (without **-r** or **-q** switch) the query will be populated from top 1000 sites.  
*Also, don't forget that query (and answer) validity is not important, what is important is the fact that we got an answer and how fast that happened.*
