1. I tried many times to set up a VPC so that I could add compute instances to the application with a predictable IP address and without using a public IP address. However, when I tried to start my instances with a VPC ID specified, Eucalyptus responded that VPC instances were not supported. So far, the private IP addresses are predictable. How can I avoid giving my instances a public IP address? Only two or three of them need public IPs.
2. I've configured 100 GB volumes attached to m3.xlarge instances for kal3a's databases and indexes. My ansible scripts can start another instance of these as needed as the project grows. Should I be making different calculations? Larger disks? If we need larger instances, I can attach the volumes to larger instances, but it will be a bigger hassle to try to resize the volumes.
3. I wanted to set up load balancers for my clustered database and index instances, but there doesn't appear to be a way to set up a load balancer that is only on the private network. While I can secure these services by configuring security groups to only expose the ports on the private IPs, the load balancers on Eucalyptus appear to force the services to be on public IPs even if I don't want or need them to be.
4.