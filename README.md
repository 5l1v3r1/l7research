# l7research
A repository (soon project) containing my Layer7 DDoS Research from HTTP Floods to Proxy Bypasses
> Contact Me: https://twitter.com/FuckBinary | https://t.me/trespassed

> Other Research: https://github.com/scaredos/cfresearch

# DDoS Prevention
In some cases, the website is the face of your company. Your website going down due to a DDoS attack, can lead to a bad reputation, lost profit, and lost customers. If your company's website is under attack, consider the following:

## Using a CDN 
Using a CDN, such as CloudFlare, or [FluxCDN], will provide help from website suffering DDoS. If you do consider a CDN, make sure you cache your webpages. Caching is the primary use of the CDN in this case. However, if you choose CloudFlare, make sure you read my research papers on cloudflare and how to protect against cloudflare ddos attacks. 
> Research Papers: https://github.com/scaredos/cfresearch

## Limit Connections
Another way to fix DDoS attacks against website is via limiting connections. With the usage of previous logs, or knowledge of how many visitors you expect, set a limit in the range of 100+ of that (If you get 20 customers, limit to 100-200). You never know when someone might promote your webpage and you receive a lot of more customers.
> NGINX Guide: [NGUIDE] | Apache Guide: [AGUIDE]

## Rate Limiting
Rate limting isn't very effective for defense against most attacks, but it can be useful in some cases. Most DDoS attacks are through the usage of infected servers or bots. These bots mainly do the attacking for the attacker, and rate limiting will be useless. If a attacker has 9,000 bots, and those 9k bots will flood your webpage, rate limtiing will stop them from connection more than once. In this instance, limiting connections and using a CDN are very effective. On the other hand, if the attacker is using a script which creates 10,000 connections to your server within a second, rate limiting is actually useful. You can set a rate limit of 10r/s (10 rates per second) and the server will only be able to connect 10 times within that second. 
> Guide: [RGUIDE]

-- End of DDoS Prevention

# Basic Layer7 Attacks 
- HTTP-GET  | Flood of GET requests 
- HTTP-POST | Flood of POST requests
- HTTP-HEAD | Flood of HEAD requests
- HTTP-KILL | Flood of GET,POST,HEAD requests
These are the most common and basic types of Layer7 DDoS attacks. They involve no hard coding or study at all to do. They simple flood the target server with the coresponding request. 
> To Patch: CDN, Limit Connections, Rate Limit

# Advanced Layer7 Attacks
- HTTP-KILL     | HTTP Flood 
- HTTP-NULL     | NULL headers
- HTTP-GOOGLE   | Uses Google Referrer to down websites
- HTTP-RAND     | Random HTTP data 
- HTTP-PATH     | Floods specific path
- HTTP-BURST    | HTTP Flood in bursts
- JSBypass-GET  | JavaScript Bypass - GET
- JSBypass-POST | JavaScript Bypass - POST
- JSBypass-HEAD | JavaScript Bypass - HEAD 
- CFBypass-GET  | CloudFlare Bypass - GET
- CFBypass-POST | CloudFlare Bypass - POST
- BFBypass-GET  | BlazingFast Bypass - GET 
- BROWSER       | Automatic Bypass (CF, BF, Sucuri, JS, etc)
- SLAVIC        | Random Data w/ Proxies, Bursts, and Bypasses

These are some of the many advanced layer 7 DDoS attacks. These take time and skill to discover and code (sometimes). They do advanced floods with malformed data and bypasses that all look like legit traffic. In most cases, these are done from one server with the usage of proxies to hide the identity of the real attacker. The proxies allow cover and higher attack scalability, since some websites block certain ISPs and VPS/VDS providers.
> To Patch: CDN, Limit Connections, Rate Limt, Block Proxies/TOR, DDoS Protection Services (CloudFlare Magic Transit, CloudFlare, BlazingFast, [FluxCDN] (Paid), Sucuri (Paid)


[FluxCDN]: https://fluxcdn.com
[NGUIDE]: https://nginx.org/en/docs/http/ngx_http_limit_conn_module.html
[AGUIDE]: https://stackoverflow.com/questions/3389496/how-do-you-increase-the-max-number-of-concurrent-connections-in-apache
[RGUIDE]: https://meta.stackexchange.com/questions/164899/the-complete-rate-limiting-guide/164900
