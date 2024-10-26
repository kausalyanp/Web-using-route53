# Website-using-route53
Create a simple website and host it using route 53. Server is ubuntu and cloud is AWS

---
Steps to follow:
---
1. Create a VPC
2. Create public subnet
3. Create route-tables, internet-gateway
4. Configure Route table, Internet Gateway and Subnets
5. Create an public Ec2 instance in public subnet in ubuntu OS
6. Install apache2 webserver
```
sudo su -
apt update
apt install apache2
systemctl enable apache2
systemctl status apache2
```
8. Purchase a domain on Godaddy or any other provider
9. Create hosted-zone with the domain name in Route53 - enter your domain name
10. Coppy the Name-Server records into the domain provider (there are 4 records, copy them all, do not add . at the end)
![image](https://github.com/user-attachments/assets/b52e0086-6520-42f7-bebe-16c315c5ff1f)
11. Create a record in your route53 hostedzone - Record type is A, enter the public ip address in value box.
12. Browse application with the your domain name.

---
Notes:
---
1. File name should be index.html
2. Check for security groups http and ssh should be enabled.
3. Record type is A and Enter the ip address in value, TTL seconds can be 60, routing policy is simple routing.
4. Wait for route53 to respond, browsing through domain name might take little time
