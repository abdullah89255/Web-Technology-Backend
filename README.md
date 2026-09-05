# Web-Technology-Backend
These technologies are important because, in modern web security, you are often testing **applications built with PHP, Python, Node.js, Java, or .NET**, while **REST and GraphQL** are the interfaces through which the browser/mobile app communicates with the backend.

The key goal for bug bounty is **not to become an expert in all seven**. You want to understand how each works, how requests flow through it, and where security controls can fail.

---

# 1. PHP

**PHP (PHP: Hypertext Preprocessor)** is a server-side programming language widely used for websites and web applications.

![Image](https://images.openai.com/static-rsc-4/J4WQkEkQnQdFfIeTmdGkhE-9UaV5PfelAlIQQU7bDzcc4u0Mdp5ZCtFSSIDMaSSgJdSb_vtNx1B3-x2kY7Pd_UafkF3bobiPKxsPnfj02lnKcvLMs2p-M7l3fINNgVvRaWVMG2Mo10EwR27453A5894oRCOdwNXd_8u9ubtoHnXg7DH4Ks0KeA9mwXXgfPGR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/lirV3jSOU5j5a-NirLlNqYXJeoHQkf88Hwk8UNy6qO6UcvHBB8JSBXWszNNAFuqk-hhR1kBEUjeHeTl__wjLuUm6vA4VhJFdo2rbQpFshMrZfDbOYHrFo7ur589L0SZLBbryodk7-AwQK8iBbHKSIrYh8rAZlqR-1dmp1Zt6nO0USlmEsQgt0zi1Vrch-cKF?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/CpwKQx0j9S-SM4WutlSiYYOnemt7DyTm4rn9frLiuShWZhIeyiFlTH0uAGxV3m8AjOFL5TQRLT7SJfCC7BHYSSrLT-X5QD9vT2Jnxvr5tG9jR9PF-tJSC_GAgYGBfGpDVBbB910ikOGC7jl_AGvrfnZ2mvjBDymxPXP3q0rbbqphhbdy_xRJ7xoDVz7qTJdu?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/el6aQMS66VBCAwGG1lDU7JnMA6GVFN7JFDWLHZ3hTn2fEaLal9YqHeV93x5s_0NJLwnr3jZB0RpraA3eUoZpSnerFrfrD-BV1chnKebbv1_eCc0G0K2zl7C1FlMJ31NCbpsSyS7qxQpD2gZh082kE60gcqmxKW2mkQY2kpBX6UlsScF_PXhh0-nZ6V9NC-nq?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/_mw3cq2qDWAPQ7wsbRKdWfb5PPhpgGqQTc03lcWV-IDKOsbSiZ6F58tSIP_9byS0cn8JfvFnbblUOGYSVjIoeJR98mQxYq2lLlDfrtlQrNO0DRX6Z3QMSUsVd-3IO8nGUEQhMH7CY5Y1pLYDKdvUxiaZgsHTSDf879IWayl2clYLWajyJYSp9DsIxsWQ4uwA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ai6lXRvO77kst24ZP8oIHrcwxlwLadCwlRH8WtJ3kIFZMtdMjJHka3XkMsyBkeGJ9rubv9rnT6mnQSyKGOIxMPeO9CqEaprdQroO4EYdf9og0MQ7uGPkSdCwBdPIEmRoyJuJJr38CdaytaMk9mjEaHxejWZi_Vj_DunsLvXrAWOX4TJyi8kjWVWi3blgQKc1?purpose=fullsize)

### Basic architecture

```text
Browser
   ↓
HTTP Request
   ↓
Web Server
   ↓
PHP Application
   ↓
Database
   ↓
PHP generates response
   ↓
Browser
```

Example:

```php
<?php

$name = "Mamun";

echo "Hello " . $name;

?>
```

The browser doesn't normally receive the PHP source code. It receives the generated output:

```html
Hello Mamun
```

### PHP is commonly used with

```text
PHP
 ├── Apache / Nginx
 ├── MySQL / MariaDB
 ├── PostgreSQL
 └── Frameworks
      ├── Laravel
      ├── Symfony
      └── CodeIgniter
```

### Security concepts to understand

When studying PHP security, learn:

* SQL injection
* XSS
* File inclusion
* File upload
* Path traversal
* Command injection
* Session management
* Authentication
* Authorization
* PHP deserialization
* Server-side request handling
* Input validation

For example, conceptually:

```php
$query = "SELECT * FROM users WHERE id = " . $id;
```

If `$id` originates from an HTTP request, the application needs proper parameterization rather than directly concatenating untrusted input.

---

# 2. Python

Python is a general-purpose programming language that's also heavily used for web development.

Popular Python web frameworks include:

```text
Django
Flask
FastAPI
Tornado
```

![Image](https://images.openai.com/static-rsc-4/V5X7HkLoLmKyNP7VA8wFVf65vVLyYus9SD44e1LP2q2Medrash8Tdg3X0P45kfbsbhoIkMrX_PgEHcnC0iOsI037bTUV_CKKVic3e-OuetRzwukmoWKGv8EF7XqoHnanpj0WhAqCCsBTjKukqtxT4XbYZUkx5_o9GIBGaml9IJEEDY10CEKeSr9dJVQoK-gv?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/MNxiMf-04GwlYy02srOUB0aTZ-OIycsr7v9qHURHHtxAiCoYHZQae0C-lVnAC6cH-jXPI5QFaroutEDrUWr0qMKBr6Aoz1H3ibNhVC3-eKP_VoiGK2ZYoFclZSgGLcbeOYGWODmHsdtyFniRoxcw02rg_CVjECtyFuT1kFKwckPpKK8Sj8RrzLU1BOrDmw3V?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/VEokjVy-t30QBdUDL6cSse_2ArSW1B_uSLNVGvRIJZgHQPKsQS9v38bWKVAz91JBis_EG6br6G7kz_gAB915qpMriE7Zn2HO3JRUHW2a2Th50wb1UqrXWh1JZZeKEqqo8BabgSXcM7X7c37Fvu8NmmQdWb67H4wG4Cm7cIcqrXNvtfKQTFA-TKwCW5jBE9zR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/AFCIcLjWlUuz0gbdbxW8NuGuDysSoqmmskwWSdcfrRtuMej5LNTAqb7nVwswHv3lb0MJbgHLsalwR9D-Mv18EFFtfvfwUYnka5cswFIWeHKbjOnyqNiZevg4wlefMAnSajH-e4HrVjdrQ7dyKHAAxYM4hkYWgL8vwbfTNPfwslHrwqtVAhs84m0w1cMEFSO4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/RzQvfb1f1ZsQLWz6OGAxU15WeGCftI8alShYVunR7ktz-ngbxGz-GCTkD9z9MuNG8QCD7L7PUZtQkMH1bqEU4FqOFdMwzelCYdqhR416ZFTmGZnFxl-EGXAZdmw67DzSSvXuhcfRYgvgFLBUYPYZetrrwgPuNaUQ1mqtF3nxDWsyL-YjDX_VR072Nej1qFNz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6vFTsut_g9A9eQe9h4yK4HktGqZE29W_wJSm2d9yZjcvytRLl-_hSS-Kb04U7sX_pMoled4Y4Jf9F7JaMkJmnLC80iXgk0YNbuAonHZRDbaABiQkzjkVZZUQYMlGycsrBZKYWGT1EfVONpuoR6MLQ6skJ23QOKIa0hGNuqcBURw74-6AZdkViadnFgKjmM-j?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/t3ym66nD65oOrgA_Al1F1rYeoPSruK4PnkEOSY2QzPaVdrrmERicNg6ZYGku6zNSkcl-vyk-DmK80c_9RE7c0PVV_Suu3EZ5VSiwAmiGhzU8mj65MLm5_yfDqsm6m7D-O7y3-Ies0BO1rFa5dO-qm1_B5Ao0SwZ8aIrUF0t11ssnmtSkgS4VrywZ5Y6x2gZz?purpose=fullsize)

### Example

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello World"

app.run()
```

Architecture:

```text
Browser
   ↓
HTTP
   ↓
Flask/Django/FastAPI
   ↓
Python code
   ↓
Database
```

### Django

Django is a larger framework.

It provides components for:

* Authentication
* Database models
* URL routing
* Templates
* Forms
* Sessions
* Admin interface

### FastAPI

FastAPI is particularly popular for APIs.

For example:

```python
@app.get("/users/{user_id}")
def get_user(user_id: int):
    return {"id": user_id}
```

Request:

```http
GET /users/123
```

Response:

```json
{
    "id": 123
}
```

### Security concepts

For security research, understand:

* Django authentication
* Django middleware
* Flask routes
* FastAPI dependencies
* Python object serialization
* Template engines
* SQL/database interaction
* File handling
* Authentication/authorization
* CORS
* API security

---

# 3. Node.js

Node.js allows JavaScript to run **outside the browser**, particularly on servers.

![Image](https://images.openai.com/static-rsc-4/FBSW4fZZp4LhWlc_FDMWg1QG7JWK82pcVu4W8orfN0K4F-xRjAjGsvL4iEnVdnbg-rCzRax_IytaZ1cWWb0fjpnLjoyMfWQMZd0_KF747YNEC_BfV8kyYBWjlQa2NAqHLGF7g3fZy9TEXFa3WNNUJC79e0aXGkNttFo4XZghSBszvBSqy7iefT5osnwh4dKZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/0kllW2ytLZoQoggImrHJoFImHYiTYpJME-XJX9IJitP9zHyRC__aYoTlZNEgYiPRWXcORzgWN-y5c1ro-INmZjSdaEjIxqFNLXSGrX62co-oxvYynjGugwRAZggSyOLA6fQ4Io7CKn0-oZaQ5n4J-uJaxNBJyOf1NgjwlldWCqjLuRNRve3uBIoCxhEfu9qV?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/qZyLx0HGOmdNGc7giVPHMPAlMrn4R-hF0iLZjyOmtc1Ss7DRDEDJ1fN-chgN4Fqj2JOa97I5FczJCbAPEbNzykURD9fJO4C4BXskUrHFGcTXdkvWR4LyIFMx2zVE-h_WU9FLBORohXr8xDP8_ohCbnv4rHsQkMwhFpSNNEHRlUMytqdNOO8yPZ-WgUAcFWYr?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/SytguqlIPPHaf-i-l2nuKnucjS4HURkAwRwCM9OrPgbNsgzRdRnkinTWilpGuz7hK5ducq2Pheg3TUai0YIiXjGt3hqn-fi7G6ZWGmB4heCgxno_8X4jh0u6WhbkZVfBsZMbhgKUREvmhu7Ju5v4_PGi59t9VJF2KxxwjiHCR4sORqS8y0iJnXm0LzDepPwA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/to8_-ItDjkQXHjCq-7gMaDUKGqVL-7OozfKJazst2SZJGUqdlFr5qt5Fc9Gb3NYGDPgXZwhKxvs2JvZxcmJk_W4mxtzaksWPe-O9Dr801ptaHEs-n8ZrDNDVRRquKdXXArvI_S5mf6qt8lqYByUYkW_STRTMM0znwiZF9IOcB5jvog6AX7tpSqSwy5OzfOrT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/hkPErjZ5RiqldS2J93N0MREUub5ie4GAy3ycTJ56G4gfHiUIbKGSbCjhGfySo-pfHZeiHGA8W7Go7aAulMfDUaNbcxFlVUKLlCFlSaVQ8c9u5OYRe59DYCLJFqs3DxpvuJx8-dAO6P-1XLuxdAmE8_CoBn6x3onJyTv6ftvFs13pR5xt2VLpMAlo0av5ifAB?purpose=fullsize)

Normally:

```text
JavaScript
     ↓
Browser
```

With Node.js:

```text
JavaScript
     ↓
Node.js
     ↓
Server
```

### Example

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
    res.end("Hello World");
});

server.listen(3000);
```

A very common Node.js framework is **Express**.

```javascript
app.get("/users", (req, res) => {
    res.json({
        message: "Users"
    });
});
```

### Node.js ecosystem

You'll frequently encounter:

```text
Node.js
 ├── Express
 ├── NestJS
 ├── Fastify
 ├── npm
 └── JavaScript/TypeScript
```

### Security topics

Pay particular attention to:

* Prototype pollution
* Command injection
* Path traversal
* SSRF
* NoSQL injection
* XSS
* Authentication
* Authorization
* JWT
* Dependency vulnerabilities
* Server-side JavaScript
* Unsafe deserialization

Since you've previously been interested in **prototype pollution**, Node.js is especially worth studying because JavaScript objects and prototype behavior are fundamental to many Node.js applications.

---

# 4. Java

Java is widely used for large enterprise web applications.

Popular frameworks include:

```text
Spring
Spring Boot
Jakarta EE
Hibernate
```

![Image](https://images.openai.com/static-rsc-4/TdH-fBoUyorCqDTAkbt9ilsYLch7Kc1hfnjTKunutlfw8WBiGct4r5wyqrTlvPyEtVkDp8sF0dgY0A8bkkKkD3KDhLdoCTfOW5OzavMRdDQfLJDvOYGTU8jXrr9P1D7yyTS8GSAw41q8e1o7yJ1FL3tzKnIgMJgJ7C-X0rIVtqWA777xhX5idc5nCM2UsIDu?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/C4eLAWp7awfhWG7bVlEOm3ZtPQudnXXbMmtR3FNpUJJ0lwBEGGCwBjk_2ngXhE1wvEfJXWQtWUWOaaEAMT3sZBnjvnFskrHFe65E8DwpoQpsxx-PPMAJm1La8WxUodUj3al8PxxmSZp--HBlr9vcRGdcwdkydpyHX3Kbf_yH3hUDZKYB41sh66OQrGrEWtCI?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dlUKyr2nQBEo1hcGh4Ke2bPb6SX9GP63Hg2SRPWvbExI0oxDGqnMqVPN4QK-clfPfjxWRj_yRPgpq4RQyFkX-BGh2EJpdZ5BTLbyEGNkwLzAc5v5E1xDSFUZejua3RMcJOwIB8B5Q1YAPx9E6FLGsqeiEUz59jOt_cNsMThATAyzEI4rjN_2SXpLB_izFE_7?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/bQvTnt2O1U0CAjTyzsN2enGTzV3zBVK8NHa4zD51hwcG5AazI6trFodg6Aic0Jbg6xGJLo3SSsq6w2huBJszHvSjVOoU3ESeFPXmVDD_Yz7YNzhuM-72mWtfEy2TDuYfm0e4P6FvBwMIC8UpOilmjCxjSQiY9u7Hu303tvH8SaX04498NuXpLSb-uwcP3y4W?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/-1Bs7jWgAvPkvIbkUsWQWmAae__x3GLDeRPdBtZLkArD6PoGj5Z6giluTQHI1IAOtPLX3i-4Vo972G25iS_B7IDJGt9AgxgPJoKQW7CjzSqJ2F-f-6vXeDw3L19pDwrkXP7GGMlIF_7sNvrHy3-NSFYI045mrjnzM5v7JJ_Dhf2KYhOQ8_I4Rp2Aq7pyXTer?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/RCvZef3jgtYADCYj3CuLdvNzE32etEEoHzJQdt9qAv_4FEmSW7C2FPgNkgeP6Aqv0llFlVLhaOdpB_l7Qb14BJXa-YYqW0w9mhOeM-MnOq9lsI5GLiIeHAnLcWxucb4g2myca3FWLH5OSDvnoB64g5bqrqtz9xZO2xGaEnMbn70dWRxDB8CbJcvavXWgzFj-?purpose=fullsize)

Typical architecture:

```text
Browser
   ↓
Nginx / Load Balancer
   ↓
Spring Boot
   ↓
Service Layer
   ↓
Repository
   ↓
Database
```

### Simple Spring-style endpoint

Conceptually:

```java
@GetMapping("/users/{id}")
public User getUser(@PathVariable int id) {
    return userService.getUser(id);
}
```

Request:

```http
GET /users/123
```

Response:

```json
{
    "id": 123,
    "name": "Mamun"
}
```

### Security concepts

Learn:

* Spring Security
* Authentication
* Authorization
* Sessions
* JWT
* CSRF
* CORS
* SQL injection
* XXE
* Deserialization
* Expression Language
* SSRF
* Access control

Java applications can become quite complex because enterprise systems often have multiple layers.

---

# 5. .NET

**.NET** is Microsoft's development platform.

For modern web applications, you'll commonly encounter:

```text
C#
.NET
ASP.NET Core
Entity Framework Core
```

![Image](https://images.openai.com/static-rsc-4/nNPfG6-YkjTtcHIfyM5T5paFwvbYqj0RoV-RN8GCJX3YFTddW5nTRdIgCB0Xv2tdCvU5ajDi-NkMhllnVwekxr97erdmVSfM9WlRkI3eAvWp4tdv1Ad6y6WzawGKpNgwZGf5jyfg43c_X1KW46rASnAeh63xLw0Bn7eGJw52y6cOnV7cICFi7Kphftpffhii?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/KZ0MyhvSgNk1hXjVa8SnXdn6zh9dmcOz9oeQLVUyR5G_yU1PKmmqCn75IYQrmVuI58tvpdor4aVOXDWDUplz4v4_y6RkLfqljmFdViwey_Mj68lOEnOgmd1BLdt4qizGRA94odDOGGmikRA3VYlBwwElPM8H3HZSDN_PXBCT-ZMDnMU0p9ObC7rM_IZ8k9Ih?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/wwTAmoU8Afitg8udTb1TnewJosu8zkka-Qdjj4sd5YWueJLHdcEfA0OcB4EQD6H1tpTEYEscTsh0SbcgETfxbVLjDK6K_T4uwR8EdqasbSWS-dTX_Q_YdFGsoMKntUDlFI-tkge7PWayPy9wvHAoVZz6EGMDYcfdGayScjqrxT2KVcdRbz9MtgzsHP19ok3L?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6bmEFUHhXCDt7nK5SJF2gPRqHZgNIaj5Vzffzhn6nSPma9kBmsM8Ft9ihaDFpDY38RFjThH8qNpLwoJ3dC80BFZegNlngqrRAvHEuNdyiYIzCgjZLluVSEbj4TKeQuWqLT2KS_PyGznLcjusWXcSD5v4WglEpIYvLEthQpCxNJ0lHznWH4leBib6ADXTOLAj?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/O0N207JdlyU5-ItrCzyrBVSxBSFO_m6zKrgC9bYYmtWIpzctJ0GXlDIes7KW5JdAWEgWFCmETXPCK1ZWk6V4r5eCN14MPaxkj0bc3SCrl5-bHadfIyHvrn-rm94G7LnZHU96v7_G-3zT8k-2Y8X_eoNuPhNSf49ycFay9zheeNPQmwCZIZh4Vdwg-kJgZQRK?purpose=fullsize)

Example ASP.NET Core endpoint:

```csharp
[HttpGet("/users/{id}")]
public IActionResult GetUser(int id)
{
    return Ok(new { id = id });
}
```

Request:

```http
GET /users/123
```

Response:

```json
{
    "id": 123
}
```

### Common .NET technologies

```text
ASP.NET Core
MVC
Web API
Razor
Entity Framework
SignalR
Identity
```

### Security concepts

Study:

* Authentication
* Authorization
* ASP.NET Identity
* JWT
* Cookies
* CSRF
* CORS
* SQL injection
* File upload
* Path traversal
* SSRF
* Deserialization
* Server-side template issues
* Misconfiguration

---

# 6. REST APIs

REST isn't a programming language.

It's an architectural style commonly used to build HTTP APIs.

Think:

```text
Frontend
    ↓
REST API
    ↓
Backend
    ↓
Database
```

For example:

```http
GET /api/users/123
```

Response:

```json
{
    "id": 123,
    "username": "mamun"
}
```

---

## Common REST methods

| Method | Typical purpose     |
| ------ | ------------------- |
| GET    | Retrieve data       |
| POST   | Create/process data |
| PUT    | Replace resource    |
| PATCH  | Modify resource     |
| DELETE | Delete resource     |

Example:

```text
GET    /api/users/123
POST   /api/users
PATCH  /api/users/123
DELETE /api/users/123
```

---

## REST authentication

An API might use:

### Cookie

```http
Cookie: session=abc123
```

### Bearer token

```http
Authorization: Bearer <token>
```

### API key

```http
X-API-Key: <key>
```

Understanding how authentication works is extremely important for security testing.

---

# REST API Security

When testing an authorized API, ask:

### Authentication

```text
Who are you?
```

### Authorization

```text
What are you allowed to access?
```

These are different.

For example:

```text
User A → /api/users/100
User B → /api/users/200
```

A security researcher checks whether authorization is properly enforced rather than assuming that changing an identifier automatically constitutes a vulnerability.

---

## Common REST API issues

Study:

```text
BOLA / IDOR
Broken authentication
Broken authorization
Mass assignment
Excessive data exposure
Rate-limit weaknesses
Injection
Improper error handling
CORS problems
API versioning issues
Business logic flaws
```

---

# 7. GraphQL

GraphQL is an API query language and runtime.

Unlike traditional REST, where you often have many endpoints:

```text
/api/users
/api/users/123
/api/orders
/api/products
```

GraphQL commonly uses a central endpoint such as:

```text
/graphql
```

The client sends a query describing the data it wants.

![Image](https://images.openai.com/static-rsc-4/fS6tftM86aGxhLOzTMwR5CPQgarymqKmkL3ccEi8aCgNMFPnbox35A4MyKnpai0d_AKrpDFG8dPqIDlWlWoN-RYSXeKBhwM6aGyMP3InK8nHTkOyJjBgxmjvG-pCNcPwf_KtbEErUo4Vi9XfScBT6EBvHa0NmgDTRWp0dHNzt2nzv1zDf5YZuQYAhtadc2Ev?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/8exud838p4rTQ4F1wERgokjPlmdUnlsOoWDPCZGeypIxIf3UmbbG9F-H2oFoxu5w4jSz7zCotnyKtTrNG77oxfHUnoAfioJvkxYoEVJ5tbR0HatXMONsAf9S1z1m7LyI-TtOsPZzLwtQ0gz09_4KKsFNiIltwvXnZSaSI4CRmssuWGQ65Hh-_GjTv7UxYKvG?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/OrfwJjPrfzye2lABL5tSSdOCnciNPi7gMM6hqHm5hY4bjPbblgjqDLQvQFMXo4DcJcpMYKQQQ4ZQko0OiGsqKduxxYTCpSf4a2n-7YuYCImULuRX7X79LAse8vX4MzUzLtV0XEipC9fx-pYtOySS1dVNysO8f_VApUO194Mo_Aj1BoGIbrkxQzpl1uCipbBD?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/qx9YHlIt5Xo5TovcXVEGux-j22kCMBMFKdNJyVokYVL1_4PZVtu-_ITFzSun0Jx05os8x1ZE-MBQyCAW7xmUnkdyI5I7Od2H_jozuvta0lT9Sa40AkQcU8grqeXrXzcF3bTpGkMXPcYqRhdFr3WvPRP0G3_ZC78qDY0cHXiMV_DSFqKvKry6J10vBs_n_SyC?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/0Pupx3IPti_IebZic0htBiUdOIyjhZEvyU6cLpMpwmWD4tCyLIu8ZUVwDPOJXWR5pWR0ZtWaVOdgziLF8vW9aC-EFJNTUOtZTxbdHFrjO-W_OjwyQRVVqT6td9dSITDV601YeSoH6sxHM_RGYR49EnF7UEwAirvVuG2Gn7GeTnkcAy6bekz6Qgau958b6a1O?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pHh7PxGA_ErW3ZZDo0qqq6FwczWFby2gn1uG0YturaMA0OH3YUqGQ_wPK0zm1Yo6jy0JTw0sEMWtTJzn10G_zpCeXdOXeqyqaVLqacPC7spMcOjdhlwk2IGaF3xS3O9a0vTzwKwD4sxpbFcK8n7v8oifo8DIRKXaznt0H07kRDpHl_9DeObeunWG0yoGZJJN?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/xAQUjS9JhUQcRaWlBoI5btakFi6WQSQad6mpotjp1eF6McSd2VORzdlevZCwsnFkMtdM0C_seewYEjsjhuaAwUGmiBGnHA9j8QKrJ7TdlvucTvN1Tzx0G61VlJvaKyMGmImhCzI-LpdyGPzobJi1js-wsrHbwBSrAjvujUbgi_JgUFMPS6YgSe_DJUKDKgmE?purpose=fullsize)

Example:

```graphql
query {
    user(id: 123) {
        id
        username
        email
    }
}
```

The server may respond:

```json
{
    "data": {
        "user": {
            "id": 123,
            "username": "mamun",
            "email": "user@example.com"
        }
    }
}
```

---

# REST vs GraphQL

### REST

```text
GET /api/users/123
```

Response might contain:

```json
{
    "id": 123,
    "username": "mamun",
    "email": "user@example.com",
    "address": "...",
    "phone": "..."
}
```

### GraphQL

The client can request specific fields:

```graphql
query {
    user(id: 123) {
        id
        username
    }
}
```

Response:

```json
{
    "data": {
        "user": {
            "id": 123,
            "username": "mamun"
        }
    }
}
```

That's one of the major differences.

---

# GraphQL Security

For bug bounty, understand:

### Introspection

GraphQL may expose schema information describing available types, queries, mutations, and fields.

### Authorization

This is extremely important.

For example:

```graphql
query {
    user(id: 123) {
        email
    }
}
```

The application must verify that the requesting user is allowed to access that email.

### Other areas

Study:

```text
Authorization flaws
Information disclosure
Introspection exposure
Query complexity
Depth attacks
Rate limiting
Injection
Batching
Mutation authorization
Business logic
```

---

# How These Technologies Fit Together

A modern application might look like this:

```text
                    USER
                     │
                     ↓
                  Browser
                     │
              HTML/CSS/JS
                     │
                     ↓
               Fetch / AJAX
                     │
             ┌───────┴────────┐
             ↓                ↓
          REST API         GraphQL
             │                │
             └───────┬────────┘
                     ↓
                Backend
                     │
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
      PHP          Python        Node.js
       │             │             │
       └─────────────┼─────────────┘
                     ↓
                Java / .NET
                     │
                     ↓
                  Database
```

In reality, an application usually uses **one or several backend stacks**, not all of these simultaneously.

---

# What You Should Actually Learn for Bug Bounty

Don't try to learn:

> PHP + Python + Node.js + Java + .NET

at expert level.

Instead:

### Phase 1 — Learn HTTP

```text
HTTP
HTTPS
Headers
Methods
Status codes
Cookies
Sessions
JSON
```

### Phase 2 — Learn one backend deeply

I'd recommend:

**Python + FastAPI/Flask**

because it will also strengthen your Python scripting skills.

Then learn the concepts of:

```text
PHP
Node.js
Java/Spring
ASP.NET
```

enough to recognize their architecture.

### Phase 3 — Master APIs

```text
REST
 ↓
Authentication
 ↓
Authorization
 ↓
JWT
 ↓
BOLA/IDOR
 ↓
Mass Assignment
 ↓
Business Logic
```

Then:

```text
GraphQL
 ↓
Schema
 ↓
Queries
 ↓
Mutations
 ↓
Resolvers
 ↓
Authorization
 ↓
GraphQL-specific security
```

### Phase 4 — Connect everything with Burp Suite

Your workflow should eventually become:

```text
Browser
   ↓
Developer Tools
   ↓
Identify API
   ↓
Burp Proxy
   ↓
Inspect Request
   ↓
Understand Backend
   ↓
Understand Authentication
   ↓
Understand Authorization
   ↓
Form Hypothesis
   ↓
Test in authorized scope
   ↓
Document Evidence
```

**The most important takeaway:** for web security, you don't need to identify the exact programming language before you can test an application. Learn to recognize **HTTP behavior, application architecture, API design, authentication, authorization, input handling, and business logic**. Those skills transfer across PHP, Python, Node.js, Java, and .NET.
