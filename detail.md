# Maipu Multi-service converged gateway Unauthorized access vulnerability
1.First direct access to the background page (http://xxxx/home/index.html), and use burp intercept packets, in turn release the packet
```
/home/index.html
```
2.During this process, the /cookie.cgi interface request packet is displayed. After the packet is discarded, you can directly enter the background and view and modify the data.
![image](https://github.com/GYWF/1/assets/35076979/8c9ad22e-01f2-4b7e-bd9c-5ac824af6130)

