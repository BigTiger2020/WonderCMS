# WonderCMS  
* Exploit Title: WonderCMS 3.1.3 - 'content' Persistent Cross-Site Scripting  
* Vendor Homepage: https://www.wondercms.com/  
* Version: 3.1.3  
   
* Stored Cross-site scripting(XSS):  
Stored XSS, also known as persistent XSS, is the more damaging of the two. It occurs when a malicious script is injected directly into a vulnerable web application. Reflected XSS involves the reflecting of a malicious script off of a web application, onto a user's browser.   

* Attack vector:  
This vulnerability can results attacker to inject the XSS payload in Page description and each time any user will visits the website, the XSS triggers and attacker can able to steal the cookie according to the crafted payload.  

* Vulnerable Parameters: Page description.  
* Steps-To-Reproduce:  
1. Go to the Simple website builder.  
2. Put this payload in Page description: "haha"><img src=x onerror=confirm('xss')>"  
3. Now go to the website and the XSS will be triggered.  

*POC  
