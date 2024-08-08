## Application Load Balancers | How to create an internet facing load balancer in AWS?
https://www.youtube.com/watch?v=pfWd-XNRY7c

## connect a public-facing load balancer to EC2 instances that have private IP addresses
https://www.youtube.com/watch?v=9Ut0cEWV9NQ

## EC2 instance attached to a load balancer is showing Unhealthy status
Unhealthy indicates that the health check is failing for the instance.

Things to check:

1. Check that the instance is running a web server
2. Check that the web page at / path responds with a valid 200 response
3. Check that instance has a security group that permits access on Port 80 (HTTP)