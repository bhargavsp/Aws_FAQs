# Routing the web server traffic from Public server to the Private server

## Access webapp running in private subnet through bastion host
Use SSH port forwarding over your bastion to the instance, assuming the bastion can access the port on the web server. See the "Local tunnels" section. Your command will look something like this: ssh -L 8080:your-webserver-ip:5000 ip-of-your-bastion -N; then, in your browser, navigate to http://localhost:8080/

`ssh -L 8080:your-webserver-ip:5000 ip-of-your-bastion -N`

https://stackoverflow.com/questions/48668239/aws-vpc-access-webapp-running-in-private-subnet-through-bastion-host 