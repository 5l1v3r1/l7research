# l7research
A repository (soon project) containing my Layer7 DDoS Research from HTTP Floods to Proxy Bypasses
> Contact Me: https://twitter.com/FuckBinary | https://t.me/trespassed | SmallDoink#0666

> Other Research: https://github.com/scaredos/cfresearch

# DDoS Prevention
In some cases, the website is the face of your company. Your website going down due to a DDoS attack, can lead to a bad reputation, lost profit, and lost customers. If your company's website is under attack, consider the following:

## Using a CDN 
Using a CDN, such as CloudFlare, or [FluxCDN], will provide help from website suffering DDoS. If you do consider a CDN, make sure you cache your webpages. Caching is the primary use of the CDN in this case. However, if you choose CloudFlare, make sure you read my research papers on cloudflare and how to protect against cloudflare ddos attacks. 
> Research Papers: https://github.com/scaredos/cfresearch

## Limit Connections
Another way to fix DDoS attacks against website is via limiting connections. With the usage of previous logs, or knowledge of how many visitors you expect, set a limit in the range of 100+ of that (If you get 20 customers, limit to 100-200). You never know when someone might promote your webpage and you receive a lot of more customers.
> NGINX Guide: [NGUIDE] | Apache Guide: [AGUIDE]













[FluxCDN]: https://fluxcdn.com
[NGUIDE]: https://nginx.org/en/docs/http/ngx_http_limit_conn_module.html
[AGUIDE]: https://stackoverflow.com/questions/3389496/how-do-you-increase-the-max-number-of-concurrent-connections-in-apache
