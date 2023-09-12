---
title: "Dockerfile Scan"
---

---

#### Dockerfile掃描是容器化領域中的一個重要安全實踐。它涉及分析Dockerfile的configuration，這是用於構建Docker容器的腳本，可以透過以下工具來尋找潛在的安全漏洞。

選擇Dockerfile掃描工具：
有幾種工具可用於掃描Dockerfile以查找安全問題。一些流行的工具包括：

* Trivy：一個簡單而全面的容器和其他工件的漏洞掃描工具。
* Clair：用於靜態分析應用程序容器中的漏洞的開源項目。

#### Dockerfile Compliance
* Least Privilege User
* No Dist Upgrade
* No Duplicate Alias
* No Healthcheck
* No Maintainer
* No Orphan Package Update
* No Self Referencing Copy From
* No Ssh Port
* No Sudo Run
* Only One Cmd
* Only One Entrypoint
* Only One Healthcheck
* Port Out Of Range
* Purge Apk Package Cache
* Purge Dnf Package Cache
* Purge Microdnf Package Cache
* Purge Yum Package Cache
* Purge Zipper Cache
* Standardise Remote Get
* Use Apt Auto Confirm
* Use Apt No Install Recommends
* Use Copy Over Add
* Use Slash For Copy Args
* Use Specific Tags
* Use Workdir Over Cd
* User Absolute Workdir

https://avd.aquasec.com/misconfig/dockerfile/general/\


#### Trivy Demo


```
trivy config ./Dockerfile
```
