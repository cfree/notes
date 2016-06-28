# Server Farm to Table: How the Internet Works

Jenna Zeigen, Digital Ocean
http://jenna.us/at-dinosaur-js

1. IP address lookup (IP of server you're trying to talk to)
1. Check cache
1. Call get hostByName call (in /etc/hosts file)
1. Local DNS server (ISP or override, ex: Google)
1. Go out and find IP of domain
1. Open a socket (HTTP default port 80)
1. Establish connection to web server (SYN, SYN-ACK, ACK)
	1. More than one connection will be opened
	1. TCP has congestion control, is constrained by the speed of light
1. TLS is more complicated than TCP connection/handshake
1. ...

Manic, hard to keep up!

gzip is a popular compression method, removes repeated info, compresses up to 70%

## HTTP 1.1 

Limited number of concurrent connections leads to bottleneck
`defer` attribute to script to make wait until all things are loaded
`async` load/processed in parallel

JS can edit CSSOM and DOM, so it will be blocked until CSS is downloaded. (Render-blocking resources)

CSSOM/DOM trees combined in render tree

Elements in the render tree should corellate to the DOM tree, but its not a 1:1 relationship

Layout is a recursive process. Render that has changed uses dirty flag system. Only dirty regions are re-painted

When fully parsed, DOM is labeled as "interactive." Scripts marked as deferred are executed, document is marked as complete and load event marked as fired.


## HTTP 2.0

Many performance tricks won't be necessary anymore


Takeaways:
- Learn how painting process works if using animations












