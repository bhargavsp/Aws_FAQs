https://d1.awsstatic.com/whitepapers/aws-web-hosting-best-practices.pdf


## Can I put nginx on public subnet and the webserver[s] on private subnet of AWS VPC?
Using a proxy or load balancer in a public subnet and your web servers in a private subnet is a best practice. In general, you should be exposing as few servers/services as possible.

I'd recommend using an Application Load Balancer or a Network Load Balancer, unless you have some specific need for an Nginx front end. You'll need multiple Availability Zones for an ALB or NLB

Also, ALB and NLB are AWS managed services, so you don't need to spend resources monitoring your reverse proxy (NGINX) for failure scenarios.
https://stackoverflow.com/questions/56103086/can-i-put-nginx-on-public-subnet-and-the-webservers-on-private-subnet-of-aws-v

## AWS Networking (VPC) From Public Server to Private Server using SSH and SCP command line
https://medium.com/@AnnAnidumaka/aws-networking-vpc-from-public-server-to-private-server-using-ssh-and-scp-command-line-9124eb5b007c