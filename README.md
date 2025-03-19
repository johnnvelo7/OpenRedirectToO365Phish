# OpenRedirectToO365Phish
From Open Redirect Vulnerability to Office 365 phishing via EvilProxy

The attacker sent a malicious email to an employee. The email contained a link to a vulnerable site, where a vulnerability in the server's API allowed unauthorized redirection. This was exploited to redirect the recipient to a phishing site for credential theft. The email was initially delivered but later flagged and removed by Microsoft Defender via Zero-hour Auto Purge (ZAP). The attacker used a mix of legitimate and phishing links, along with image attachments, to enhance credibility. Despite Defender’s intervention, any user interaction before removal posed a security risk.


![image](https://github.com/user-attachments/assets/6dfe4189-3355-4312-b214-563c19737b0e)

![image](https://github.com/user-attachments/assets/4f52022b-5b3f-4778-86e1-9f61118ecf47)

## How did this happen?

An attacker can manipulate the "redirecturl" parameter in the CRM API to redirect users to arbitrary websites. This can be exploited for phishing attacks, malware distribution, or credential theft.

CRM API Endpoint: /crm10/api/public/runworkflow

![image](https://github.com/user-attachments/assets/37b7757b-87bf-40cf-a6d0-cf592fc5bbaa)

Example:
https://crm.workwisesoftware.com/crm10/api/public/runworkflow?workflow=ClickThru&activityid=https://velosecurity.com=doc&entityname=Contact&includecrmkeys=True&eventcode=CLICKSITE&redirecturl=https://velosecurity.com

