# Network Load Balancer Hands-On
![image](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/8977a6e8-d8ab-48b3-acf5-0ee68355ea6a)
## Note!!
Choose a Network Load Balancer when you need ultra-high performance, TLS offloading at scale, centralized certificate deployment, support for UDP, and static IP addresses for your applications. Operating at the connection level, Network Load Balancers are capable of handling millions of requests per second securely while maintaining ultra-low latencies.

In this hands-on exercise, we'll set up a Network Load Balancer (NLB) on AWS to evenly distribute TCP traffic across multiple EC2 instances. Let's dive in:

## Step 1: Set up EC2 Instances

First, we'll need to create two EC2 instances and ensure they're running and accessible. Make sure to allow HTTP traffic in the security group settings.

![Instance Both](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/af5ed0cd-1843-4600-acd5-712a97599f0d)
![Instance 1](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/e3c6318c-401a-4900-8e5f-f604d7ca4fc9)
![Instance 2](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/fd2020ae-6293-4132-a74c-b2a9c4dcce64)

## Step 2: Configure Network Load Balancer

Navigate to the Load Balancer section in the AWS Management Console and choose "Network Load Balancer."

![Load Balancer](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/ffb27cf6-1267-47f2-98a4-3965cd75eae8)

## Step 3: Create Target Group

During configuration, create a target group with HTTP and add the EC2 instances to it.

![Target Group Configuration](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/8f4fb723-47ca-4e36-a1c4-18192e05a903)

Select the EC2 instances you created to balance.

![Select EC2 Instances](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/9130b351-1bc0-4689-8df1-f20e3b0213e7)

## Step 4: Testing NLB Functionality

Once the NLB is created, copy the DNS name and paste it into the browser. Verify that both EC2 instances are running and responsive.

![Load Balancer Done](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/f6e3cdb2-92bd-4e9e-a544-4cd191acc6bc)

![Load Balancer Running](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/0349c3d8-6189-4839-91e3-870cee857df5)
![Load Balancer Running](https://github.com/RimshaAzmat/NetworkLoadBalancer-HandOn/assets/144583193/e6d3a516-ceb4-4575-912a-d863faf342cd)


That's it! You've successfully set up and tested a Network Load Balancer on AWS. Ensure that the load balancer evenly distributes traffic across both EC2 instances, even if one becomes unhealthy or is terminated.
