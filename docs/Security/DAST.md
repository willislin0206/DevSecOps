---
title: "DAST"
---

---
#### DAST 動態應用程序安全測試（Dynamic Application Security Testing），是一種用於應用程序安全測試的自動化技術。DAST在測試期間模擬攻擊者攻擊應用程序，通過發送各種請求來測試應用程序的安全性。

#### DAST測試可以自動化測試對象的訪問權限、注入攻擊、跨站腳本（XSS）攻擊、跨站請求偽造（CSRF）攻擊、文件包含漏洞等常見安全漏洞。通常DAST測試是通過一些軟件或者線上工具完成的，如OWASP ZAP、Burp Suite、Netsparker等。

#### DAST測試與靜態代碼分析（Static Code Analysis）不同，靜態代碼分析是通過對代碼的檢查來發現安全漏洞，而DAST則是通過模擬攻擊來測試應用程序的安全性。

##### 特色：

#### 1. 模擬攻擊：DAST測試通過模擬攻擊者的攻擊來發現應用程序中的漏洞。它可以測試各種攻擊，例如SQL注入、跨站腳本攻擊、跨站請求偽造攻擊等。

#### 2. 自動化測試：DAST測試是自動化的，可以自動化發現應用程序中的安全漏洞，減少了手動測試的工作量和錯誤率。

#### 3. 快速測試：DAST測試可以在短時間內測試大量的頁面和功能，這使得它成為一種快速且有效的安全測試方法。

#### 4. 客戶端測試：DAST測試是在客戶端進行的，這意味著它可以測試實際運行的應用程序，而不是測試代碼。

#### 5. 與靜態分析結合：DAST測試可以與靜態分析結合使用，以提高測試的準確性和完整性。

總的來說，DAST測試是一種快速、自動化、客戶端和模擬攻擊的安全測試方法，可以有效地發現應用程序中的安全漏洞

#### Owasp Zap

OWASP ZAP（Zed Attack Proxy）是一種開源的應用程序安全測試工具，可以用於發現應用程序中的安全漏洞和漏洞。ZAP提供了許多功能，包括被動和主動測試、自動化攻擊、漏洞管理、報告生成等等。

#### 1. 開源免費：ZAP是一款開源免費的應用程序安全測試工具，所有人都可以自由使用和修改它的源代碼。

#### 2. 都跨平台支持：ZAP可以在Windows、Linux和MacOS等操作系統上運行。

#### 3. 網絡代理：ZAP可以作為一個網絡代理，捕獲HTTP和HTTPS請求，檢查請求和響應的內容，從而發現安全漏洞和漏洞。

#### 4. 被動和主動測試：ZAP支持被動和主動測試。在被動測試中，ZAP會通過攔截和分析瀏覽器和應用程序之間的通信來發現漏洞。在主動測試中，ZAP將向應用程序發送各種請求，測試應用程序的安全性。

#### 5. 自動化攻擊：ZAP可以自動化攻擊，例如SQL注入攻擊、XSS攻擊、文件包含攻擊等等。

#### 6. 漏洞管理：ZAP可以幫助管理應用程序中發現的漏洞，跟踪漏洞的狀態、進度和優先級。

#### 7. 報告生成：ZAP可以生成各種類型的報告，例如HTML、XML、PDF等等，幫助管理和開發人員快速了解應用程序的安全狀況。

#### Architeture

![not found](./../assets/DAST/browser-network-proxy.png)

#### Baseline Scan 
which runs the ZAP spider against the target for (by default) 1 minute followed by an optional ajax spider scan before reporting the results of the passive scanning.

**Demo**
This is a Demo
##### Use OWASP ZAP image 
```
docker pull owasp/zap2docker-stable
```
##### Run the container
```
docker run it owasp/zap2docker-stable bash
```
##### Baseline to scan  
```
docker run 
```


#### Full Scan 
which runs the ZAP spider against the target (by default with no time limit) followed by an optional ajax spider scan and then a full active scan before reporting the results.

**Demo**
This is a Demo

#### API Scan 
which performs an active scan against APIs defined by OpenAPI, or GraphQL (post 2.9.0) via either a local file or a URL.

**Demo**
This is a Demo.........................................


#### Default Policy Rule

**主動掃描**

* Admin Console - Detected
* Apache Struts - Remote Code Execution - CVE-2017-5638
* Backup and Old Files
* Blind SQL Injection
* Buffer Overflow
* CRLF Injection
* Client-side Cross-Domain Script Inclusion
* Client-side HTTP Parameter Pollution
* Clickjacking
* Content Security Policy Header Not Set
* Cookie No HttpOnly Flag
* Cookie Without Secure Flag
* CORS Misconfiguration
* Cross-Domain JavaScript Source File Inclusion
* Cross-Site Flashing
* Cross-Site Scripting (DOM based)
* Cross-Site Scripting (Reflected)
* Cross-Site Scripting (Stored)
* Database Disclosure
* Debug Errors
* Directory Browsing
* Email Addresses Disclosure
* External Redirect
* File Inclusion
* File Path Manipulation
* Forced Browsing
* HTTP Method Not Allowed
* HTTP Parameter Override
* HTTPoxy
* Improper Error Handling
* Improper Filesystem Permissions
* Improper Neutralization of CRLF Sequences
* Insecure Communications
* Insecure Cryptographic Storage
* Insecure HTTP Method
* Insecure Randomness
* Insecure Storage of Passwords
* Insufficient Anti-automation
* Insufficient Authorization
* Insufficient Session Expiration
* Insufficient Transport Layer Protection
* LDAP Injection
* Local File Inclusion
* Local Resource Inclusion
* MIME Type Mismatch
* OS Command Injection
* OWASP Top 10 2007
* OWASP Top 10 2010
* OWASP Top 10 2013
* OWASP Top 10 2017
* Path Traversal
* Password Autocomplete in Browser
* PHP Injection
* PHP Object Injection
* Plaintext Storage of a Password
* Private IP Disclosure
* Remote OS Command Injection
* Remote File Inclusion
* Server-side Code Injection
* Server-side Request Forgery
* Session Fixation
* SQL Injection
* Stack Trace Disclosure
* Struts-Shock
* Suggestive File Download
* Unvalidated Redirects and Forwards
* Unvalidated Web Forms
* Username Enumeration
* WebDAV Detection
* XPath Injection


**被動掃描**
* Cross-Domain Script Inclusion: 
檢測網站是否存在可能允許來自不同來源的腳本在網頁中執行的漏洞。
* Cross-Domain Resource Policy:
檢測網站是否設置了跨域資源共享（CORS）策略來限制來自不同來源的資源的訪問權限。
* Cross-Origin Resource Sharing (CORS) Header Not Found: 
檢測網站是否未設置CORS標頭，從而可能允許來自其他域的資源訪問網站資源。
* Directory Listing Enabled: 
檢測網站是否啟用了目錄列舉功能，使攻擊者可以輕鬆地瀏覽網站上的文件和目錄。
* External JavaScript libraries loaded over HTTP: 
檢測網站是否加載了未加密的JavaScript庫，可能存在安全漏洞。
* HTTP Header Injection Detected (HTTP Response Splitting): 
檢測網站是否存在HTTP響應分裂漏洞，允許攻擊者注入惡意標頭到HTTP響應中，從而可能導致跨站腳本攻擊等安全問題。
* Incomplete or No Cache-control and Pragma HTTP Header Set: 
檢測網站是否未完整設置HTTP標頭，可能導致瀏覽器快取不正常。
* Insecure Password Fields: 
檢測網站是否在未加密的頁面上顯示了用戶名和密碼，可能被攻擊者竊取。
* Missing X-Content-Type-Options Header: 檢測網站是否未設置X-Content-Type-Options標頭，可能導致MIME型別混淆攻擊。
* Multiple Content-Type Headers: 檢測網站是否存在多個Content-Type標頭，可能導致MIME型別混淆攻擊。
* Multiple Content-Security-Policy Headers Found: 
檢測網站是否存在多個Content-Security-Policy標頭，可能導致安全策略不正常。
* No Access-Control-Allow-Origin Header Found: 
未發現 Access-Control-Allow-Origin 響應頭，可能導致跨站請求偽造攻擊（CSRF）等安全問題。
* No Content-Security-Policy Header Found: 
未發現 Content-Security-Policy 響應頭，可能導致跨站腳本（XSS）攻擊等安全問題。
* No X-Content-Type-Options Header Found: 
未發現 X-Content-Type-Options 響應頭，可能導致 MIME-sniffing 攻擊等安全問題。
* No X-Frame-Options Header Found: 
未發現 X-Frame-Options 響應頭，可能導致點擊劫持攻擊等安全問題。
* No X-XSS-Protection Header Found: 
未發現 X-XSS-Protection 響應頭，可能導致跨站腳本（XSS）攻擊等安全問題。
* Password Autocomplete Detected: 
檢測到密碼自動填充，可能導致安全問題。
* Private IP Disclosure: 
檢測到應用程式可能會洩漏內部網路 IP，可能導致攻擊者獲取內網機器的資訊。
* Referrer Leakage: 
檢測到引用網址洩漏，可能導致敏感資訊外洩。
* Script Passive Scan Rule: 
被動檢測 JavaScript 檔案中可能存在的安全漏洞。
* Session ID in URL Rewrite: 
偵測到 URL 中包含 Session ID 且被重寫，可能導致會話劫持攻擊等安全問題。
* Session ID in URL Rewrite - Path Disclosure: 
偵測到 URL 中包含 Session ID 且被重寫，可能導致資訊洩漏安全問題。
* Unencrypted Login Form: 
檢測到登入表單使用未加密的傳輸協定，可能導致帳號密碼被攻擊者竊取。
* Unencrypted Login Form over SSL: 
檢測到登入表單使用 SSL 加密但無法強制使用，可能導致安全問題。
* Weak Authentication Parameters: 
檢測到弱的認證參數，可能導致身份驗證繞過等安全問題。
* Weak Password Policy: 
檢測到弱的密碼策略，可能導致密碼被破解或其他安全問題。