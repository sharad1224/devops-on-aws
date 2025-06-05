# Global Accelerator

***Launch EC2 in Mumbai Region***
![243](https://github.com/user-attachments/assets/c94c4b02-0929-4eb5-a63f-1cff283c6875)

***Host a Static Website***
![244](https://github.com/user-attachments/assets/95a73788-0480-415e-a170-2e3cb03f854e)

## Use this user data script or run manullay command

```bash
#!/bin/bash
sudo yum install httpd -y
sudo echo "<h1> Welcome to AWS : Mumbai - server " >> /var/www/html/index.html
sudo systemctl enable --now httpd
sudo systemctl restart httpd
```
***Launch another EC2 in Different Region Like US***
![245](https://github.com/user-attachments/assets/81eb4964-12e7-4427-9c95-b6fbfb2c2269)

***again Host a Static Website***
![246](https://github.com/user-attachments/assets/d347342f-283d-4c54-ba6c-7477e3f0286e)

## Use this user data script or run manullay command

```bash
#!/bin/bash
sudo yum install httpd -y
sudo echo "<h1> Welcome to AWS : US(Ohio) - server " >> /var/www/html/index.html
sudo systemctl enable --now httpd
sudo systemctl restart httpd
```

***Go to Global Accelerator sevice***
![247](https://github.com/user-attachments/assets/3eec0b55-dd0f-4b58-be7f-3f2987eb4b19)

***Create accelerator***
![248](https://github.com/user-attachments/assets/9a02ab74-9750-49fc-acdb-758ce94040f2)
![249](https://github.com/user-attachments/assets/e8efee83-65e3-40b2-8728-238f61801bcf)
![250](https://github.com/user-attachments/assets/19094a9b-d241-4df9-8eb0-1a57948acfdb)
![251](https://github.com/user-attachments/assets/9847f47e-28fa-4cdd-9e75-f70940d11c49)
![252](https://github.com/user-attachments/assets/788496b7-c4d5-41e6-b2d3-8b1a59879a14)
![253](https://github.com/user-attachments/assets/704b0543-ad86-452a-98d5-9012e0ef813b)
![254](https://github.com/user-attachments/assets/75381b90-d99c-4302-83d7-e3dd7b313d45)

***Select own accelerator and Wait for Deploying, take time to 4-5 min***
![255](https://github.com/user-attachments/assets/89a12196-57c5-4bd9-bae5-7eb5086e7882)

***Also wait for Healthy Endpoint***
![256](https://github.com/user-attachments/assets/79e4577f-d327-4b0b-adda-ebb9f69606b0)

***after Deploying & Healthy to copy a DNS name***
![257](https://github.com/user-attachments/assets/bfb2146b-a532-4a69-91d3-0b6193b090b6)

***paste the link and show the output for your nearest Web server***
![258](https://github.com/user-attachments/assets/cb09cb8a-fe0b-4290-a768-60ba857b2c1c)

***Use **proxysite.com** web or **VPN** for US network and paste the link, now fetch the nearest Web server*** 
![259](https://github.com/user-attachments/assets/84aa3bf3-7b64-431d-8212-93e89bc0c36b)
