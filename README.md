# UdacityProject-Udagram-WebApp
Deploy a High-Availability Web App using CloudFormation

![digram](https://github.com/mo-qassem/UdacityProject-Udagram-WebApp/blob/d4565ed2ba9f4468a0d243bca71e18c94e30819a/Diagram.png)

**TheNextBigThing** [Udagram](http://Udagram-ALB-434827795.us-east-1.elb.amazonaws.com)

 **Extra:**

  1. Added VPC endpoint (Gateway) to provide secure access from app subnet to s3 bucket "udacity-static-web-site-demo" to download the web application files to app instances.
  2. Added Bastion instance for management purposes.
  3. created ASG with a dynamic scaling policy (simple scaling) to add elasticity to our infrastructure.
  4. Installing CWAgent on app instances to collect custom metrics and log files like apache web server access logs.
     *There is an issue with collectd package as it is not available with apt repos.
  5. Securing CWAgent configuration and private key part for the Bastion instance at System Manager "Parameter Store" and retrieving it securely using AWS CLI on our local machine.
