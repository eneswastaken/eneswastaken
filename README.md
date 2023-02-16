┌─[jeff@matrix] - [/home/jeff] - [2020-07-25 10:39:57]
└─[0] <> curl -I https://camo.githubusercontent.com/1dc7d7611b4dbdca4b54c6cacdd2823f1bce4fca/68747470733a2f2f6a7274656368732e6e65742f6170692f726563656e745356472e7376673f
HTTP/1.1 200 OK
Connection: keep-alive
Content-Length: 2411
Cache-Control: public, max-age=2678400
Content-Security-Policy: default-src 'none'; img-src data:; style-src 'unsafe-inline'
Content-Type: image/svg+xml
Server: github-camo (62249a1c)
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type-Options: nosniff
X-Frame-Options: deny
X-Xss-Protection: 1; mode=block
X-GitHub-Request-Id: 1640:4307:11CC6D:159A5E:5F1C443D
Accept-Ranges: bytes
Date: Sat, 25 Jul 2020 14:48:42 GMT
Via: 1.1 varnish
Age: 525
X-Served-By: cache-mdw17377-MDW
X-Cache: HIT
X-Cache-Hits: 2
X-Timer: S1595688523.694051,VS0,VE0
Vary: Accept-Encoding
X-Fastly-Request-ID: 7a621c4d10b3ee434e4f55a05b04a059c6a64fbe
Timing-Allow-Origin: https://github.com
Github enables you to clear the Camo cache for a single image using the curl PURGE command. This is a nice hack if you merely want to update an external image in your readme that got updated; however, you don’t want to do this every time your dynamic component is updated. If the image is serving as a page visit counter, the purge call would have to be sent every time the image is fetched.

┌─[jeff@matrix] - [/home/jeff] - [2020-07-25 10:48:42]
└─[0] <> curl -X PURGE https://camo.githubusercontent.com/1dc7d7611b4dbdca4b54c6cacdd2823f1bce4fca/68747470733a2f2f6a7274656368732e6e65742f6170692f726563656e745356472e7376673f
{ "status": "ok", "id": "4942-1591860663-32446227" }
