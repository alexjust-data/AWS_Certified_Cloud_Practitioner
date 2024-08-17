

## AWS Certified Cloud Practitioner CLF-C02

- [AWS Certified Cloud Practitioner CLF-C02](#aws-certified-cloud-practitioner-clf-c02)
  - [What is a Cloud Computing?](#what-is-a-cloud-computing)
  - [IAM - Identity and Acces Management](#iam---identity-and-acces-management)
    - [IAM Policies inheritance](#iam-policies-inheritance)
    - [IAM Policies Hands On](#iam-policies-hands-on)
    - [IAM – Password Policy](#iam--password-policy)
    - [IAM MFA Hands On](#iam-mfa-hands-on)
      - [CLI \& SDK](#cli--sdk)
    - [AWS CloudShell](#aws-cloudshell)
    - [IAM Roles for AWS Services](#iam-roles-for-aws-services)
    - [IAM Roles Hands On](#iam-roles-hands-on)
    - [IAM Security Tools](#iam-security-tools)
    - [IAM Security Tools Hands On](#iam-security-tools-hands-on)
    - [IAM Guidelines \& Best Practices](#iam-guidelines--best-practices)
    - [Shared Responsibility Model for IAM](#shared-responsibility-model-for-iam)
    - [IAM Section – Summary](#iam-section--summary)
  - [EC2 - Elastic Compute Cloud](#ec2---elastic-compute-cloud)
    - [EC2 - Basics](#ec2---basics)
    - [Create EC2 Instance with EC2 UserData to have a WebSite](#create-ec2-instance-with-ec2-userdata-to-have-a-website)
    - [EC2 Instance Types Basics](#ec2-instance-types-basics)
    - [Security Groups \& Classic Ports Overview](#security-groups--classic-ports-overview)
    - [Security Groups Hands On](#security-groups-hands-on)
    - [SSH Overview](#ssh-overview)
    - [EC2 Instance Connect](#ec2-instance-connect)
    - [EC2 Instance Roles Demo](#ec2-instance-roles-demo)
    - [EC2 Instances Purchasing Options](#ec2-instances-purchasing-options)
    - [Shared Responsibility Model for EC2](#shared-responsibility-model-for-ec2)
    - [EC2 Section – Summary](#ec2-section--summary)
  - [EC2 Instance Storage](#ec2-instance-storage)
    - [About EBS Multi-Attach](#about-ebs-multi-attach)
    - [EBS Hands On](#ebs-hands-on)
    - [EBS Snapshots Overview](#ebs-snapshots-overview)
    - [EBS Snapshots Hands On](#ebs-snapshots-hands-on)
    - [AMI Overview](#ami-overview)
    - [AMI Hands On](#ami-hands-on)
    - [EC2 Image Builder](#ec2-image-builder)
    - [EC2 Instance Store](#ec2-instance-store)
    - [EFS – Overview](#efs--overview)
    - [Shared Responsibility Model for EC2 Storage](#shared-responsibility-model-for-ec2-storage)
    - [Amazon FSx Overview](#amazon-fsx-overview)
    - [EC2 Instance Storage - Summary](#ec2-instance-storage---summary)
    - [Section Cleanup](#section-cleanup)
  - [Elastic Load Balancing \& Auto Scaling Groups Section](#elastic-load-balancing--auto-scaling-groups-section)
    - [Elastic Load Balancing (ELB) Overview](#elastic-load-balancing-elb-overview)
    - [Application Load Balancer (ALB) Hands On](#application-load-balancer-alb-hands-on)
    - [uuu](#uuu)
---
We will cover 40 AWS services (out of the 200+ in AWS)
Sample question : Certified Cloud Practitioner
https://explore.skillbuilder.aws/learn/course/external/view/elearning/14050/aws-certified-cloud-practitioner-official-practice-question-set-clf-c02-english

**Creating an AWS free Account** (with new email addres)
To have your account activated, make sure to:
* Add a Payment Method
* Verify your phone number
* Choose an AWS Support Plan (Free)

Your account will be activated when you receive an email like this: `When your 12 month free usage term expires or if your application use exceeds the tiers, you simply pay standard, pay-as-you-go service rates (see each service page for full pricing details). For more details, see the offer terms.` 

Details can be found here: https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/

---
### What is a Cloud Computing?

**What is a server composed of?**

![](/img/03/02.png)

**What is Cloud Computing?**
* Cloud computing is the on-demand delivery of compute power, database storage,
applications, and other IT resources
* Through a cloud services platform with pay-as-you-go pricing
* You can provision exactly the right type and size of computing resources you need
* You can access as many resources as you need, almost instantly
* Simple way to access servers, storage, databases and a set of application services
* Amazon Web Services owns and maintains the network-connected hardware required for these application services, while you provision and use what you need via a web application.

**The Deployment Models of the Cloud**

`Private Cloud:` 
* Cloud services used by a single organization, not exposed to the public.
* Complete control
* Security for sensitive applications
* Meet specific business needs

`Public Cloud:`
* Cloud resources owned and operated by a third- party cloud service provider delivered over the Internet.
* Six Advantages of Cloud Computing

`Hybrid Cloud:`
* Keep some servers on premises and extend some capabilities to the Cloud
* Control over sensitive assets in your private infrastructure
* Flexibility and cost- effectiveness of the public cloud

**The Five Characteristics of Cloud Computing**
`On-demand self service:` Users can provision resources and use them without human interaction from the service
provider
`Broad network access:` Resources available over the network, and can be accessed by diverse client platforms
`Multi-tenancy and resource pooling:` Multiple customers can share the same infrastructure and applications with security and privacy • Multiple customers are serviced from the same physical resources
`Rapid elasticity and scalability:` Automatically and quickly acquire and dispose resources when needed • Quickly and easily scale based on demand
`Measured service:` Usage is measured, users pay correctly for what they have used

**Six Advantages of Cloud Computing**
`Trade capital expense (CAPEX) for operational expense (OPEX)` Pay On-Demand: don’t own hardware. ReducedTotal Cost of Ownership (TCO) & Operational Expense (OPEX)  
`Benefit from massive economies of scale`: Prices are reduced as AWS is more efficient due to large scale  
`Stop guessing capacity` : Scale based on actual measured usage  
`Increase speed and agility`  
`Stop spending money running and maintaining data centers`  
`Go global in minutes`: leverage the AWS global infrastructure  

**Problems solved by the Cloud**
• `Flexibility`: change resource types when needed  
• `Cost-Effectiveness`: pay as you go, for what you use  
• `Scalability`: accommodate larger loads by making hardware stronger or adding additional nodes  
• `Elasticity`: ability to scale out and scale-in when needed  
• `High-availability and fault-tolerance`: build across data centers  
• `Agility`: rapidly develop, test and launch software applications  

**Types of Cloud Computing**

`Infrastructure as a Service` **(IaaS)**    
• Provide building blocks for cloud IT  
• Provides networking, computers, data storage space • Highest level of flexibility  
• Easy parallel with traditional on-premises IT  
`Platform as a Service` **(PaaS)**  
• Removes the need for your organization to manage the underlying infrastructure • Focus on the deployment and management of your applications  
`Software as a Service` **(SaaS)**  
• Completed product that is run and managed by the service provider  

![](/img/03/03.png)

**Example of Cloud ComputingTypes**

`Infrastructure as a Service:`  
* Amazon EC2 (on AWS)  
* GCP, Azure, Rackspace, Digital Ocean, Linode  
  
`Platform as a Service:`  
* Elastic Beanstalk (on AWS)  
* Heroku, Google App Engine (GCP), Windows Azure (Microsoft)  
  
`Software as a Service:`
* Many AWS services (ex: Rekognition for Machine Learning)
* Google Apps (Gmail), Dropbox, Zoom

**Pricing of the Cloud – Quick Overview**
![](/img/03/05.png)

**AWS Global Infrastructure**  
https://infrastructure.aws/  
• AWS Regions
• AWS Availability Zones
• AWS Data Centers
• AWS Edge Locations / Points of Presence

**How to choose an AWS Region?**
If you need to launch a new application, where should you do it?  
• `Compliance` with data governance and legal requirements: data never leaves a region without your explicit permission  
• `Proximity` to customers: reduced latency  
• `Available` services within a Region: new services and new features aren’t available in every Region  
• `Pricing`: pricing varies region to region and is transparent in the service pricing page  

**AWS Availability Zones**

* Each region has many availability zones (usually 3, min is 3, max is 6). Example:`ap-southeast-2a • ap-southeast-2b • ap-southeast-2c
* Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
* They’re separate from each other, so that they’re isolated from disasters
* They’re connected with high bandwidth, ultra-low latency networking

Content is delivered to end users with lower latency

**Tour of the AWS Console**
`AWS has Global Services:`  
• Identity and Access Management (IAM)  
• Route 53 (DNS service)  
• CloudFront (Content Delivery Network)   
• WAF (Web Application Firewall)  
`Most AWS services are Region-scoped:`  
• Amazon EC2 (Infrastructure as a Service)  
• Elastic Beanstalk (Platform as a Service) • Lambda (Function as a Service)  
• Rekognition (Software as a Service)  
`Region Table` : https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services  

**Tour of the Console & Services in AWS**

All services

![](/img/03/06.png)

One feature I really appreciate is the search bar. You can type in a service, such as `Route 53`, and it will provide you with search results. Typically, it will show you four services that match your query. Within these services, you can also explore related features—13 features match Route 53, for instance. This allows you to directly access the domain names of the Route 53 service, which is quite convenient. Additionally, you can access blogs, knowledge articles, documentation, and more. This is a very useful tool.

Now, let's delve into Route 53 to explore its console. This console is unique because, in the top right-hand corner, it displays "global." 

![](/img/03/07.png)

This indicates that the console does not require region selection, which is an exception rather than the norm. Some AWS services are known as global services, meaning that no matter where you are, you will see the same view. However, if you switch to another service, such as EC2, you'll notice that the top right-hand corner now displays a specific region, like Ireland. This means that if you are operating the console in Ireland or another region, such as Canada, the resources you see will differ. That's why it's crucial to stay within the same region throughout this tutorial and course.

Another important resource is the [AWS global infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/), which you can find through a quick Google search. This provides a wealth of information about AWS services. One particularly valuable tool is the [AWS Regional Services](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/?p=ngi&loc=4) list, which shows the availability of services by region. For example, if I mention a service during the course and you don't see it in your region, you can check this list to find out where it is available. You can look up Cape Town, for instance, to see which services are available there. If you don't see a particular service, you may need to switch your region in the console to access it, as not all AWS services are available in every region.

**Shared Responsibility Model diagram**

https://aws.amazon.com/compliance/shared-responsibility-model/

![](/img/03/08.png)

**AWS Acceptable Use Policy**

https://aws.amazon.com/aup/

• No Illegal, Harmful, or Offensive Use or Content 
• No Security Violations
• No Network Abuse
• No E-Mail or Other Message Abuse


### IAM - Identity and Acces Management

**IAM: Users & Groups**

IAM = Identity and Access Management, Global service
• `Root account` created by default, shouldn’t be used or shared
• `Users` are people within your organization, and can be grouped
• `Groups` only contain users, not other groups
Users don’t have to belong to a group, and user can belong to multiple groups


Let's take an example. We have an organization with six people: 

![](/img/03/09.png)

Alice, Bob, Charles, David, Edward, and Fred. All of these individuals are part of your organization. Alice, Bob, and Charles work together as developers, so we’ll create a group called "Developers" that includes Alice, Bob, and Charles. Similarly, David and Edward work together, so we’ll create an "Operations" group for them. Now, we have two groups within IAM.

It's important to note that IAM groups can only contain users, not other groups. This is a critical point to understand—groups can only contain users, not other groups. Additionally, it's possible for some users not to belong to any group. For instance, Fred is not assigned to a group. While this isn't best practice, it is something you can do in AWS. Moreover, a user can belong to multiple groups. For example, if Charles and David also work together on your audit team, you could create a third group for them. In this scenario, Charles and David would be part of two different groups. These are some of the possible configurations for IAM.

Now, why do we create users and groups? The primary reason is to grant them access to your AWS accounts. To do this, we need to assign them permissions. Users and groups can be assigned a JSON document, known as an IAM policy. 

Let me show you an example. 

![](/img/03/10.png)

This policy document isn't programming; it simply describes, in plain English, what a user or a group of users is allowed to do.

For instance, through this policy, we can specify that users are allowed to access the EC2 service, use the Elastic Load Balancing service, and interact with CloudWatch. We’ll cover what EC2, Elastic Load Balancing, and CloudWatch are later, but the key point here is that this JSON document allows us to define what services our users can access in AWS.

These policies are crucial for defining user permissions. In AWS, it's essential not to grant everyone unrestricted access, as this could lead to significant costs or security issues. Instead, AWS follows the principle of least privilege, which means you only grant users the permissions they need to perform their tasks. If a user only needs access to three services, you should create a permission set that allows access to just those services.

**IAM Users & Groups Hands On**

In the search bar, I just type "IAM" and go into the IAM console. Upon arriving at the IAM dashboard, we see some security recommendations that we can, for now, ignore. What I want to draw your attention to is the "Users" option on the left-hand side. This is where we're going to create users for IAM. But first, let's notice something. If you go to the top right corner and click on "Global," you’ll see that the region selection is not active. This means that IAM, as an entire service, is a global service, and therefore, there's no region to be selected. When you create a user in IAM, it will be available everywhere. However, some other consoles we'll see in this course will be region-specific. Just something to keep in mind.

Okay, so now we have users. And why do we create users? Well, we create users because right now, we are using what's called the root user. If you click on this, you’ll see there’s just the account ID available to you.

![](/img/03/11.png)

When you see this, it means you’re using the root account, and it's not best practice to use the root account. Therefore, we want to create users, such as admin users, that will allow us to use our accounts more safely. So let's go ahead and create a user. 

I will provide a username, for example, "Nuria". Of course, I want to give myself access to the Management Console, so I'm going to do this. We have the option to use Identity Center, which is recommended, or to create an IAM user. I will choose the second option because it is simpler, and from an exam perspective, this is the one you need to know about. But don't worry, this does not affect how your course is going to go.

![](/img/03/12.png)

Okay, so we create an IAM user. Now we have to set the password. If this were a user that was not me, I would leave it as an auto-generated password and keep the option requiring the user to change their password at the next sign-in. But because it’s me, I'm just going to enter a custom password and untick this option because I don't want to change my password at the next login. Then, click on "Next."

Next, we have to add permissions to this user. We can add them directly, or we can get started with groups. Let’s create a group. 

![](/img/03/13.png)


We’ll name the group "admin" and assign the policy "administrator access." 

![](/img/03/14.png)

Now that this is done, we can add the user to the admin group. 

![](/img/03/15.png)

Click on "Next," and we can review everything: the username, the permissions on the group, and the tags. Tags are everywhere in AWS. They are optional, but they allow you to add metadata to many of your resources. For example, I could specify that "Nuria"’s `department` is `engineering`. This is not something I’m going to do in the course, but I want to show you how you can add tags to resources in AWS.

![](/img/03/16.png)

Now the user is successfully created. We can email sign-in instructions or download CSV files, and then we can log in with this user. 

![](/img/03/17.png)

But first, let's **return to the user list** and review everything. Here is Nuria user list—here. 

![](/img/03/18.png)

We also have groups. If I go to the left-hand side under "User groups," we see the "admin" group. Let’s examine it. The "admin" group has one user in it named "Nuria". 

![](/img/03/19.png)

If you look at the permissions of the "admin" group, you’ll see that "administrator access" is attached to it. 

![](/img/03/20.png)

If I go to my user "Nuria", 

![](/img/03/21.png)

we can look at the permission policies and see that it also has "administrator access." However, this permission was not attached directly to the user but via the "admin" group. This means that "Nuria" inherited all the permissions of the "admin" group. This is why we put users in groups—it simplifies managing permissions.

![](/img/03/22.png)

Now, let’s go back to our dashboard and sign in with our user "Nuria". First, we can look at our user account, which has an account ID and a sign-in URL. You can easily customize this sign-in URL by creating what's called an account alias. For example, it could be "Nuriajust"." Then click on "Create alias." The alias has to be unique, so if it’s not available, try something like "v5." Using this alias, I can simplify my sign-in URL.

![](/img/03/23.png)

To sign in using my "Nuria" account, we could use the same browser, or we could create a new browser window in private mode. The benefit of doing this is that we can have two windows side by side using AWS. If you don’t do this, that’s fine. But if you log in using the "Nuria" account on the right-hand side window, you will be disconnected on the left-hand side. This is the only difference. To use two accounts simultaneously—the root on the left and my account on the right—a trick I use is opening a private window in my web browser. Chrome, Firefox, and Safari all have this feature. By pasting the sign-in URL, as you can see, I get the sign-in as an IAM user. 

![](/img/03/24.png)

To get to this page, we can go back to one, and as you can see, when you do a sign-in on AWS, you have the option to sign in as the root user or the IAM user. To get back to this, select IAM user, then enter either the account ID or the account alias that I copied earlier. This will take you to the sign-in page. The IAM username will be "Nuria", and the password will be whatever you set earlier. Then you sign in.

The cool thing is that if I look at the top right-hand side, I am logged in using my IAM user. It displays the account ID and the IAM user. However, if I look at the top right-hand side of the other window, it just shows the account ID, indicating that it’s the root account.

![](/img/03/25.png)

And now, if I look at the top right-hand side here, it just displays the Account ID, indicating that it’s the root account. So, to summarize, we have the root account logged in on the left-hand side through a regular window, and the IAM user logged in on the right-hand side through a private window.

Please ensure you do not lose your root account credentials or your admin login information, as this could lead to significant issues with your account, requiring you to contact AWS support for assistance. Unfortunately, I cannot help you with that. From a course perspective, I recommend using your IAM user rather than your root user, but this is just general advice. Sometimes you'll see me using the root account, and other times I'll be using an IAM user. I will let you know during the course when it's necessary to use the root account or when to use an IAM user, so don't worry about that.

#### IAM Policies inheritance

Okay, let's now discuss IAM policies in depth. Imagine we have a group of developers—Alice, Bob, and Charles—and we attach a policy at the group level. In this case, the policy will be applied to every member of the group. So Alice, Bob, and Charles will all get access and inherit this policy. If you have a second group, such as operations, with a different policy, David and Edward will have a different policy from the developers' group. If Fred is a user, he has the option not to belong to any group, and we have the possibility to create what's called an inline policy, which is a policy that is only attached to a specific user. So that user could or could not belong to a group. You can create inline policies for whichever user you want.

Finally, if Charles and David both belong to the audit team, and you attach a policy to the audit team as well, Charles and David will also inherit that policy from the audit team. In this case, Charles has a policy from the developers' group and a policy from the audit team, while David has a policy from the audit team and a policy from the operations team. This should make a lot of sense when we get into the hands-on part.

![](/img/03/26.png)

**IAM Policies Structure**

Now, in terms of policy structure, you just need to know at a high level how it works and how it is named. This is something you will see frequently in AWS, so get familiar with this structure. It is a JSON document. An inline policy structure consists of a version number, which is usually 2012-10-17—this is the policy language version—an ID, which is used to identify the policy (this is optional), and one or more statements. Each statement has several important parts: the SID is the statement ID, which is an identifier for the statement and is also optional. The effect specifies whether the statement allows or denies access to certain APIs; in the example on the right-hand side, it shows "allow," but it could also be "deny." The principal defines which account, user, or role the policy applies to; in this example, it is applied to the root account of your AWS account. The action is the list of API calls that will be either denied or allowed based on the effect, and the resource is a list of resources to which the actions will be applied. In the example, it is a bucket, but it could be many different things. Lastly, there's a condition that specifies when the statement should be applied or not, but this is optional and not represented in the example.

![](/img/03/27.png)

As you prepare for the exam, make sure you thoroughly understand the effect, principal, action, and resource components. Don't worry; you'll encounter these concepts throughout the course, and you should feel confident with them by the end. That's it for this lecture. I hope you enjoyed it, and I will see you in the next lecture.

#### IAM Policies Hands On

So now let's have a look at IAM policies in depth. First of all, let's go into Users. As you can see, the user Nuria is part of the admin group and therefore has administrator access permissions to AWS. That means that if I use my user Nuria to go into the IAM console—so now I'm using my user—and then I go to the left-hand side and click on Users, as you can see, I can see my user Nuria, which is right here. My user Nuria has permission to do anything because right now it's an administrator. 

![](/img/03/28.png)

But what I'm going to do is go to the admin group, and then I'm going to remove my user Nuria from that group. By removing the user, which I've done right now, Nuria loses its permissions on the right-hand side. How do we make sure of this? Well, let's refresh this page. 

![](/img/03/29.png)
![](/img/03/30.png)

As you can see, now I see zero users, and I get an access denied, and it says that I don't have permission to do `iam:ListUsers`. Therefore, because I removed my Nuria user from the admin group, I've lost permissions to look at users on the right-hand side. 



Let's try to fix this. Let's go into IAM, and we're going to go under Users, find Nuria here. Right now, as you can see, Nuria has zero permission policies. But let's add permissions. We can add permissions directly or create an inline policy. Let's add permissions, as this will be easier. Again, we could add the user back to a group, but that's not what we want. We could attach policies directly to my user. The policy I'm going to attach is `IAM read-only access`. This will allow my user Nuria to read anything on IAM, which is what we want. Let's add this permission. Now this policy has been added. 

![](/img/03/31_.png)

Back here, let's refresh this page. 

![](/img/03/32.png)

As you can see now, I can finally do my API call again and look at the Nuria user in my Users category. I can view users. I can view user groups, such as admin. But can I create a group? Let's try to create the developer group and then create this group. As you can see, I cannot create it because I'm not allowed to create a group. I'm only given `read-only access on IAM`. Therefore, because I have read-only access, I cannot create groups. 

![](/img/03/33.png)

This shows you that you can only permission users for what they're supposed to do. Of course, if I wanted to give access to create groups on the right-hand side, I would need to attach a broader permission set, such as `IAM full access`.


Next, let's do something. I'm going to go to the left-hand side under User Groups, and I'm going to create a group. This group is going to be called Developers. I'm going to add the user Nuria to this group and attach whatever policy I can find. For example, Alexa for Business, but it doesn't really matter. Just attach the first policy you find. Let's create this group. 

![](/img/03/34.png)

![](/img/03/35.png)

Okay, this has been added. Finally, let's go into the admin group. Again, we're going to add users and re-add Nuria to this group. 

![](/img/03/36.png)

Now, if we go back to the Nuria user—let's go into IAM, look at the users, and look at Nuria—I'm going to shut down this machine on the right-hand side. 

![](/img/03/37.png)

If we look at Nuria as a user, as you can see, we have three permission policies attached to my user. We have the administrator access that has been inherited from the admin group. We have this Alexa for Business managed policy that has been attached by the developers group. And finally, IAM read-only access that has been attached directly. As you can see, I inherited different permissions based on how they were attached. 

![](/img/03/38.png)

Now let's look at policies in detail. On the left-hand side, let's look at policies. First, let's have a look at this administrator access policy. 

![](/img/03/39.png)

If we look at it, it's the permission that gave us administrator access to everything. If you look at the permissions defined in this policy, as a summary, you can see this allows all the services in AWS. This number can change over time, but it doesn't matter. The course will be up to date. All these services, for example, App Mesh, Alexa for Business, or Amplify, all have full access. How is this permission defined? If you click on JSON, this is the JSON form of this policy. 

![](/img/03/40.png)

We can see that here we have allow, action star, and resource star. Star in AWS means anything. It means we allow any action on any resource. Allowing any action on any resource is the same as giving administrator access to someone. This is how it's been defined. 

![](/img/03/41.png)

Let's look at another policy, for example, the IAM read-only access that we saw before. If we look at it, we see that IAM is authorized with `full list and limited read` in **Acces level**. 

![](/img/03/42.png)

If I click on it, you can actually see all the API calls that have been allowed as part of this policy, which is very handy. But if we look at how this has been defined, let's click on JSON. Here we have the JSON document that shows how this has been defined. 

![](/img/03/43.png)

The effect is allow. Then we list the API calls that are allowed. We have this one, this one, and then we have `"iam:Get*",`. When you have `get star`, it means that anything that starts with get and then has something after it is authorized, for example, get users or get groups. The same goes for list, so we have list star, meaning list users or list groups. By using a star, we encompass and group many API calls together. All this is allowed on resource star. That summarizes what the read-only IAM access policy is made up of. This is very handy. 

You can also create your own policy. Let's create a policy. We have a visual editor or a JSON editor. 

![](/img/03/44.png)

If you have JSON, you can simply edit this and create your JSON document with this builder, which is very handy. Or you can use the visual editor. For example, let's say IAM. 

![](/img/03/45.png)

We want to create stuff for IAM. What action do we want to authorize? We want to authorize list users. 

![](/img/03/46.png)

We're going to take this and `get user` —just two API calls. 

![](/img/03/47.png)

As you can see, we have selected one out of 38 in list and one out of 32 in read. Then what do we want to authorize this on? On all resources or only specific resources? 

![](/img/03/48.png)

This is a very simple one, but as you can see, this builder is very handy. When you click on Next, you can look and say `My IAM Permissions`, and then we create this policy. 

![](/img/03/49.png)

If we look at the policy we created, 

![](/img/03/50.png)

we can look at the corresponding JSON and see that, indeed, through the visual editor, we allowed IAM list users and IAM get user on resource star. 

![](/img/03/51.png)

This policy can be attached to groups, users, and so on. This is how you manage permissions in AWS. To wrap up this hands-on, let's go to User Groups, and we're going to delete the Developers group because we don't need it. 

![](/img/03/52.png)

Then I'm going to go into my Nuria user, and I'm going to remove this IAM read-only access that I had attached directly. Now Nuria only belongs to the admin group and has administrator access. Of course, if I go back to my IAM console here and just look at users, as you can see, yes, everything is showing fine, so it is working correctly.

![](/img/03/53.png)

---

#### IAM – Password Policy

Now that we have created users and groups, it is time to protect these users and groups from being compromised. For this, we have two defense mechanisms.  The first one is to define what's called a password policy. Why? Well, because the stronger the password you use, the more security you have for your accounts. 

Strong passwords = higher security for your account.  

In AWS, you can setup a password policy:  

• Set a minimum password length  
• Require specific character types: • including uppercase letters  
• lowercase letters  
• numbers  
• non-alphanumeric characters  
• Allow all IAM users to change their own passwords  
• Require users to change their password after some time (password expiration)  
• Prevent password re-use  

In AWS, you can set up a password policy with different options. The first option is to set a minimum password length, and you can require specific character types. For example, you may want to require an uppercase letter, a lowercase letter, a number, and a non-alphanumeric character, such as a question mark, and so on. Then you can allow or prevent IAM users from changing their own passwords. Additionally, you can require users to change their password after a certain period to enforce password expiration. For example, you could require users to change their passwords every 90 days. Finally, you can also prevent password reuse, ensuring that users don’t change their passwords to the one they already have or to one they had before. This is great because a password policy is really helpful against brute force attacks on your accounts.

**Multi Factor Authentication - MFA**
But there's a second defense mechanism that you need to know about, especially for the exam, and that is multi-factor authentication (MFA). You may have already used it on some websites, but on AWS, it is a must, and it is highly recommended to use it. Users have access to your account, and they can potentially do a lot of things, especially if they are administrators. They can change configurations, delete resources, and perform other actions. Therefore, you absolutely want to protect at least your root account and, ideally, all your IAM users. So, how do we protect them in addition to the password? By using an MFA device.


• Users have access to your account and can possibly change configurations or delete resources in your AWS account
• You want to protect your Root Accounts and IAM users
• MFA = password you know + security device you own


![](/img/03/54.png)

• Main benefit of MFA: if a password is stolen or hacked, the account is not compromised

So, what are the MFA device options in AWS? You need to know them for the exam, but don't worry, they are quite simple. The first option is a virtual MFA device. This is what we will use in the hands-on portion, and you can use apps like Google Authenticator, which works on one phone at a time, or Authy, which supports multiple tokens on a single device. With a virtual MFA device, you can have your root account, your IAM user, another account, and another IAM user all on the same device. You can have as many users and accounts as you want on your virtual MFA device, making it a very convenient solution.

---

**MFA devices options in AWS**

What is MFA? MFA involves using a combination of something you know, like a password, and something you own, like a security device. These two factors together provide much greater security than just a password alone. For example, let's consider Alice. Alice knows her password, but she also has an MFA-generating token. By using these two factors together when logging in, she can successfully authenticate with MFA. The benefit of MFA is that even if Alice's password is stolen or hacked, the account will not be compromised because the hacker would also need to have access to Alice's physical device, such as her phone, to log in. Obviously, this is much less likely to happen.

Next, we have a Universal Second Factor (U2F) security key. This is a physical device, such as a YubiKey by Yubico, which is a third-party product not provided by AWS. A physical device like this is easy to use; you simply attach it to your keychain, and you're good to go. The YubiKey supports multiple root and IAM users using a single security key, so you don't need to carry multiple keys for different users, which would be a hassle.

![](/img/03/55.png)

---

**MFA devices options in AWS**

There are other options as well. You can use a hardware key fob MFA device, such as one provided by Gemalto, which is also a third-party product. Finally, if you are using AWS GovCloud in the US, there is a special key fob provided by SurePassID, also a third-party product.

![](/img/03/56.png)

That's the theory on how to protect your account. In the next lecture, we will implement these security measures. I will see you in the next lecture.

---

#### IAM MFA Hands On

So we are going to first define a password policy. For this, click on Account Settings on the left-hand side. `IAM` > `Account Settings` You will find `Password Policy`, and you can edit it. 

Here, we can use the IAM default password policy, which consists of these kinds of requirements, 

![](/img/03/57.png)

or we can customize the password policy and enforce a minimum password length. We can also require an uppercase letter, a lowercase letter, a number, and a non-alphanumeric character. We can also enable password expiration, for example, setting it to expire after 90 days, or requiring an administrative reset upon expiration. Additionally, we can allow the user to change their own password or prevent password reuse. This password policy can be edited directly from the IAM console, and that's the first part of security.

![](/img/03/58.png)

---

The second part involves setting up multi-factor authentication (MFA) for your root account. To do this, click on the account name and then on `Security Credentials`. 

![](/img/03/60.png)

If you are logged in as the root user, you will see My Security Credentials for the root user. There is a way to protect your root user, which is the most important account in your AWS account, by using multi-factor authentication. 

Now, just so you know, I'm going to demonstrate how it works in front of you, but I've had students who locked themselves out of their accounts because they lost access to their multi-factor authentication device. As such, if you think you are at risk of losing your iPhone or whatever device you use, do not do this, okay? Just keep your phone with you, and watch my explication; that will be good enough. If you want to practice along with me, you can, and you can also delete the MFA device after activating it.

![](/img/03/61.png)

Okay, but let's go ahead and assign an MFA device. I will call this one "myiPhone" because this is what I have, but you can name it whatever you want. Then you can select the type of MFA device. It could be an Authenticator app, which is what I'm going to use, but it can also be a security key or a hardware TOTP token. I'm going to use an Authenticator app because it will be virtual. Now we proceed with the app setup. 

![](/img/03/62.png)

**Virtual authenticator apps** There's a [list of compatible applications](https://aws.amazon.com/iam/features/mfa/) for Android and iOS that we know work well with AWS. I'm going to use the `Twilio Authy Authenticator`, which is an app I like. 

![](/img/03/63.png)


What I have to do then is launch the app on my phone and click on **Show QR code**. 

![](/img/03/64.png)

When you display the QR code, you need to scan it directly on your phone. To do this, you add an account and scan the QR code here. Once scanned, it will add the account and start naming it. We will just save this, and it looks good. Then we get access to MFA codes. The first MFA code is 301935, which is generated by my iPhone in real time, and this code is going to change over time. The reason why these two codes are asked by AWS is to ensure that the MFA device is set up correctly and that the codes are accurate. The second code is 792843, and of course, it will be different for your device. Once these two codes are entered, you click on Add MFA. As you can see, we can register up to eight MFA devices currently, and you can scroll down and see them on the list. The multi-factor authentication (MFA) device called "my iPhone" has been created right now. If you want to remove it, you can remove it, and so on.

![](/img/03/65.png)

**How can users access AWS ?**
* To access AWS, you have three options:
  * AWS Management Console (protected by password + MFA)
  * AWS Command Line Interface (CLI): protected by access keys
  * AWS Software Developer Kit (SDK) - for code: protected by access keys

* Access Keys are generated through the AWS Console
* Users manage their own access keys
* Access Keys are secret, just like a password. Don’t share them • Access Key ID ~= username
* Secret Access Key ~= password

Example (Fake) Access Keys

![](/img/03/66.png)


##### CLI & SDK

**What’s the AWS CLI?**

• A tool that enables you to interact with AWS services using commands in your command-line shell
• Direct access to the public APIs of AWS services
• You can develop scripts to manage your resources
• It’s open-source https://github.com/aws/aws-cli
• Alternative to using AWS Management Console

So if you're new to the cloud, programming, or IT in general, you might not know what a CLI is. CLI stands for Command Line Interface, and the AWS CLI is a tool that allows you to interact with AWS services using commands from your command line shell. Whenever you see some code where you type a command line and then it returns results, for example, aws s3 cp and so on, this is what we call the CLI. We use the AWS CLI because we start every command with the word "aws".

With this CLI, you get direct access to the public APIs of your AWS services, which is going to be very helpful in this course. Using the CLI, you can develop scripts to manage your resources and automate some of your tasks. The CLI is open-source, and you can find all the source code on GitHub. It is an alternative to using the AWS Management Console. I know that some people actually do not even use the Management Console; they only use the CLI, for example.


![](/img/03/67.png)


**What’s the AWS SDK?**

• AWS Software Development Kit (AWS SDK)
• Language-specific APIs (set of libraries)
• Enables you to access and manage AWS services programmatically
• Embedded within your application
• Supports
• SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
• Mobile SDKs (Android, iOS, ...)
• IoT Device SDKs (Embedded C, Arduino, ...)
• Example: AWS CLI is built on AWS SDK for Python


So what’s the AWS SDK? [SDK stands for Software Development Kit](https://aws.amazon.com/developer/tools/). This is a set of libraries that is language-specific, so you're going to have an SDK for different programming languages. Similarly, it will allow you to access and manage your AWS services and APIs programmatically. However, the SDK is not something that you use within your terminal; it is something that you embed within your application that you have to code. Your application will include the AWS SDK. 

It supports many different programming languages, such as JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++, and others. There's also the mobile SDK if you're using Android or iOS, and the IoT (Internet of Things) device SDK in case you're using some thermal sensors, bike locks, or other connected devices.

To give you an example of what you can build with the SDK, the AWS CLI that we're going to be using in this course is actually built on the AWS SDK for Python named Boto.

In the next lecture, we're going to practice setting up the CLI and dealing with access keys. 


**AWS CLI Setup on Mac**

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

1. In your browser, download the macOS pkg file:  https://awscli.amazonaws.com/AWSCLIV2.pkg

If you have installed correctly, open de terminal and show de version
```sh
➜  ~ aws --version
aws-cli/2.17.30 Python/3.11.9 Darwin/23.3.0 exe/x86_64
```

So let me show you how to create access keys. I will click on my username, Nuria, and go to Security Credentials. I will scroll down and create an access key. 

![](/img/03/68.png)

As you can see, there are some selections you need to make, and based on the selection I'm making—for example, if I want an access key for the CLI—AWS is going to provide alternative recommendations. For example, for the CLI, it's better to use Cloud Shell, which I will show you in the next lecture, so don't worry about it, or to use CLI v2 with authentication through the IAM Identity Center, which I won't show you because it's a bit more complicated. Based on what you want to do—whether it's local code, an application running outside of AWS, in AWS, and so on—you will have some recommendations at the bottom.

For now, we're going to use the CLI, and we'll use these access keys. I'll click here to acknowledge that I understand the above recommendations, but I still want to create an access key because it is important for you to understand how they work and what they are. 

![](/img/03/69.png)

So let's create this access key, and now this is the only time you'll be able to access the access key and the secret access key.

![](/img/03/70.png)

Now, I'll go back to a previous version of that lecture where you see the old UI, but don't worry, nothing changes from that point on. The first thing I have to do is configure my AWS CLI, so I'm going to type `aws configure` on terminal, and then I'm prompted to enter my access key ID. Very nice. I can just enter this one and press Enter, and then I'm prompted to enter my secret access key, which I will enter right here as well. The default region name is the region that is closest to you. I will choose us-east-1 because I will be doing all my tutorials in us-east-1, but you should choose your own region. You can enter your own region name, and by the way, you can get the region name directly from this dropdown right here. It shows you the name of the region as well as the region code. So for me, I'm going to use us-east-1. I'll press Enter, and for the default output format, I'll just press Enter as well.

```sh
➜  ~ aws configure              
AWS Access Key ID [****************AGQD]: AKIASFIXCXAFSSIT7GS
AWS Secret Access Key [****************tiAp]: Wa3mydyvQR4tlEqq/+a7qKIfFQySjJWelBQP3r
Default region name [eu-central-1]: eu-west-1
Default output format [json]: 
```

So now Nuria AWS CLI is configured, and we can see how it works. We can do aws iam list-users and press Enter, and this will list all the users in my account. As we can see, the user I have right now is called Nuria. Here is the user ID, here is the ARN, when it was created, and when the password was last used, which is very similar to what I would get if I were to go into this UI right here. The Management Console and the CLI provide similar kinds of information.

Having multiple IAM users in an AWS account is a common and recommended practice. Each user can have different permissions and credentials. The fact that both "Alex" and "Nuria" exist as users in the account does not mean they are using the same credentials. It simply means that both users have been created in the AWS account.

```sh
➜  ~ aws iam list-users   

{
    "Users": [
        {
            "Path": "/",
            "UserName": "Alex",
            "UserId": "AIDASFIXCXAFSBSZAH6YO",
            "Arn": "arn:aws:iam::148761655307:user/Alex",
            "CreateDate": "2024-08-14T10:50:02+00:00",
            "PasswordLastUsed": "2024-08-14T11:40:06+00:00"
        },
        {
            "Path": "/",
            "UserName": "Nuria",
            "UserId": "AIDASFIXCXAF7F3AAWSRL",
            "Arn": "arn:aws:iam::148761655307:user/Nuria",
            "CreateDate": "2024-08-14T10:53:51+00:00",
            "PasswordLastUsed": "2024-08-14T16:43:13+00:00"
        }
    ]
}
```

Verification of the Current User:

If you want to verify that the credentials currently configured belong to Nuria, you can run the following command. This command will return information about the user or role you are currently using, based on the credentials configured in your default profile. You should see an ARN that refers to the user "Nuria" if the configured credentials belong to Nuria.

```sh
➜  ~ aws sts get-caller-identity


{
    "UserId": "AIDASFIXCXAF7F3AAWSRL",
    "Account": "148761655307",
    "Arn": "arn:aws:iam::148761655307:user/Nuria"
}
```

Next, I want to show you what happens if we remove permissions from our user. So I'm going to go to Admins, and I'm going to remove the Nuria user from the `admin` group. 

![](/img/03/71.png)

So again, if I go back to my user Nuria, it doesn't have any permissions. I did this obviously with my root account, not the other account.

![](/img/03/72.png)

Now, if I go into my UI and refresh this page, I'm going to get an error saying that I do not have permission to do this. 

![](/img/03/73.png)

But let's try to do the same thing with the CLI. So we're going to do an iam list-users call, and we get no response because it was denied. 

```sh
➜  ~ aws iam list-users         

An error occurred (AccessDenied) when calling the ListUsers operation: 
User: arn:aws:iam::148761655307:user/Nuria is not authorized to perform: iam:ListUsers on resource: 
arn:aws:iam::148761655307:user/ because no identity-based policy allows the iam:ListUsers action
```


The CLI permissions are, of course, the exact same as the permissions you get from the IAM console.

So the takeaway from this lecture is that you can access AWS using the Management Console or by using an access key and secret access key that you can configure and then use in the CLI. 

And obviously, do not forget to add your user back into the group; otherwise, that would be horrible. So I'm going to go into Groups, Admins, and I'm going to add my Nuria user back into my group. Now I am an administrator again. So that's it. I will see you in the next lecture.

![](/img/03/74.png)

---

#### AWS CloudShell

https://docs.aws.amazon.com/cloudshell/latest/userguide/faq-list.html

![](/img/03/76.png)

![](/img/03/77.png)

![](/img/03/78.png)


#### IAM Roles for AWS Services

* Some AWS service will need to perform actions on your behalf
* To do so, we will assign **permissions** to AWS services with **IAM Roles**
* Common roles:
  * EC2 Instance Roles
  * Lambda Function Roles
  * Roles for CloudFormation

Now, let's talk about the last component of IAM, which is called IAM roles. Some AWS services that we'll be launching throughout this course will need to perform actions on our behalf, within our accounts. To perform these actions, they need permissions, just like users do. Therefore, we need to assign permissions to these AWS services, and to do that, we're going to create what's called an IAM role.

IAM roles are similar to users, but they are intended to be used by AWS services, not by physical people. This might sound a bit confusing at first, so let me explain. For example, during this course, we're going to create an EC2 instance, which is essentially a virtual server. We'll cover this in the next section. This EC2 instance might need to perform actions on AWS, and to do that, we need to give it the necessary permissions. To achieve this, we'll create an IAM role, and together, they will work as a unit.

When the EC2 instance tries to access some information from AWS, it will use the IAM role. If the permissions assigned to the IAM role are correct, the EC2 instance will be granted the access it needs to make the necessary API calls. Common roles include the EC2 instance roles that I just mentioned, as well as other roles we'll explore in this course, such as Lambda function roles or CloudFormation roles.

I understand this is a high-level overview. In the next lecture, we'll be creating a role, but we won't be using it until the following section. Let's go ahead and create a role, and I'll see you in the next lecture.

#### IAM Roles Hands On

![](/img/03/83.png)

Let's practice using roles. On the left-hand side, click on `Roles`, and you'll see that some roles may have already been created for your account. It could be two or more; it doesn't matter. What we're going to do now is create our own role. A role is a way to give AWS entities permissions to perform actions on AWS.

`IAM` > `Roles` -> Create role

![](/img/03/79.png)

As you can see, there are different kinds of roles you can create—actually, five options available right now. However, for this hands-on session and for the exam, the one you need to focus on is a role for an AWS service. So, let's choose that option. Next, we need to select the service for which this role will apply. When you click on it, you'll see commonly used services like EC2 and Lambda, or you can create a role for nearly any service on AWS. This is a fundamental aspect of AWS, and that's why we're learning about it now.

We're going to create a role for an EC2 instance, which we'll use in the EC2 section later. So, choose EC2, and the use case will be set to EC2. Ignore any other options and click Next. 

`IAM` > `Roles` > `Create role` -> Next

Now that we've selected a role for an EC2 instance, we need to attach a policy. I'll attach the IAM read-only access policy to allow my EC2 instance to read whatever is in IAM. Click Next.

![](/img/03/80.png)

Next, you need to enter a role name. I'll name mine DemoRoleForEC2. After that, you'll select the trusted entities, which essentially means that this role can be assumed by the EC2 service. This is what defines it as a role specifically for Amazon EC2. We then verify the permissions to ensure it has IAM read-only access, and finally, we create the role.

![](/img/03/81.png)

`IAM` > `Roles` > `Create role` > `Next` -> Create Rol

Now, my role is created, and it appears in my role list. We can verify that the permissions assigned to this role are correct. However, we won't be able to use this role just yet, as we need to cover the EC2 section first. But when we do get to it, we will use this role. In the meantime, you've learned how to create a role for Amazon EC2 and how to attach the correct permissions to it.

![](/img/03/82.png)

#### IAM Security Tools

IAM Credentials Report (account-level)
* a report that lists all your account's users and the status of their various
credentials

IAM Access Advisor (user-level)
* Access advisor shows the service permissions granted to a user and when those services were last accessed.
* You can use this information to revise your policies.

We’re nearing the end of this section, but before we wrap up, let's discuss the security tools available in IAM. The first tool is the IAM Credentials Report, which operates at the account level. This report will include all your account users and the status of their various credentials. We’ll generate this report shortly and review it together.

The second security tool in IAM is called IAM Access Advisor, which functions at the user level. The Access Advisor shows the service permissions granted to a user and when those services were last accessed. This tool is particularly useful when implementing the principle of least privilege, as it allows us to identify unused permissions and adjust a user's access to align with this principle.

I’ll see you in the next lecture, where we’ll go over how to use these security tools.

#### IAM Security Tools Hands On

Let's generate a credentials report. To do this, click on Credential Report on the left-hand side, and then select Download Credential Report. This action will create a CSV file. Since I'm using a training account, the report may not be particularly extensive, but we can see some important details.

![](/img/03/84.png)


In this CSV file, there are two rows: one for my root account and one for my user account, Stéphane. The report shows when the user was created, whether the password is enabled, when the password was last used and last changed, and when the next rotation is expected (if password rotation is enabled). It also indicates whether MFA is active; for example, it's active on my root account but not on my Stéphane account. Additionally, the report tells us if access keys have been generated. In my case, they were created for my Stéphane account but not for my root account. The report also provides details on when these keys were last rotated and last used, among other information.

This credentials report is extremely useful for identifying users who haven't changed or used their passwords in a while. It gives you a clear view of which users may need attention from a security standpoint.

Now, let's take a look at IAM Access Advisor. For this, I'll go to my user account, Nuria, and then click on Access Advisor on the right-hand side. 


![](/img/03/82.png)

Access Advisor will show which services have been accessed by this user and when. As you can see, my user accessed services like Organizations, Health, Identity and Access Management (IAM), EC2, and Resource Explorer by interacting with the AWS UI. However, some services, like Alexa for Business or AWS App2Container, were not accessed.

Using Access Advisor, you can evaluate whether a user has the correct permissions. For instance, if a user has access to 37 different services but only uses a few, you might consider reducing their permissions. This UI allows you to drill down into the details. For example, if a user accesses Amazon EC2, the UI shows that this access was granted by the AdministratorAccess policy.


In summary, Access Advisor is a powerful tool for managing granular user access permissions in AWS.

That’s it for this lecture. I hope you found it helpful, and I'll see you in the next lecture

#### IAM Guidelines & Best Practices

Here are some general guidelines on IAM and best practices, because I don't want you, if you go to use AWS, to make some mistakes.

* Do not use the root account except when setting up your AWS account.
* Ensure you have two accounts: a root account and your own personal account.
* Remember, one AWS user equals one physical user. Do not share your credentials with others; create separate users for them.
* Assign users to groups and manage permissions at the group level for better security.
* Create a strong password policy.
* Use and enforce multi-factor authentication (MFA) to enhance account security.
* Use IAM roles when assigning permissions to AWS services, including EC2 instances.
* If using AWS programmatically or through the CLI/SDK, generate access keys and keep them secure like passwords.
* Audit account permissions using the IAM credentials report or IAM Access Advisor.
* Never share your IAM users and access keys.

These guidelines will help you manage IAM securely and effectively in AWS.

#### Shared Responsibility Model for IAM

![](/img/03/86.png)

#### IAM Section – Summary

* **Users**: mapped to a physical user, has a password for AWS Console
* **Groups**: contains users only
* **Policies**: JSON document that outlines permissions for users or groups • Roles: for EC2 instances or AWS services
* **Security**: MFA + Password Policy
* **AWS CLI**: manage your AWS services using the command-line
* **AWS SDK**: manage your AWS services using a programming language • Access Keys: access AWS using the CLI or SDK
* **Audit**: IAM Credential Reports & IAM Access Advisor

---

### EC2 - Elastic Compute Cloud

We’re going to make sure to set up a budget and an alarm for that budget during this course to prevent unnecessary or excessive spending. To do this, start by navigating to the Billing and Cost Management console. You can find it by clicking on the top right of your screen.

![](/img/04/01.png)

As you can see, I’m getting several "Access Denied" messages because I’m logged in as an IAM user, Stéphane, with administrative access. However, even with administrative access, I cannot access billing data. To fix this, you’ll need to log in using your root account. Once you're in the root account, you’ll notice that it simply displays the name of your account without "IAM user" next to it. Click on your account name, then go to Accounts.

![](/img/04/02.png)

Scroll down until you find the option labeled IAM User and Role Access to Billing Information. As you can see, it is deactivated by default. Activate IAM access, which will allow IAM users with administrative permissions to access billing information.

![](/img/04/03.png)

Now, if I return to the billing console and refresh the page, it may take a moment, but eventually, my billing data will become visible. Except for the forecast, which may show a "data available exception" due to insufficient historical data, you should be able to see all cost-related information.


>Let me show you what a billing page looks like for an account that has incurred some costs. You’ll see details such as the month-to-date costs, the total forecasted costs for the current month, and last month’s total costs. You can also view a breakdown of costs by month, which becomes useful when analyzing your spending.
>
>To delve deeper, go to Bills. For example, if you incurred costs during December 2023 for this course, you can scroll down to find the Charges by Service section. Here, you’ll see the number of active services, such as EC2 (Elastic Compute Cloud). For instance, in my case, I have `$`43 in costs from the EU (Ireland) region, with a breakdown that includes charges for the Amazon Elastic Compute NAT Gateway (`$`35), EBS, Elastic IP, and more. This detailed bill helps you understand exactly how each service contributes to your overall cost.
>
>Next, you can explore the Free Tier option on the left-hand side. AWS offers a free tier, and this section lets you monitor your current and forecasted usage against the free tier limits. If your usage is forecasted to exceed the free tier, the dashboard will alert you in red, indicating that you will incur charges. To avoid unnecessary costs, make sure to turn off any services you no longer need.

   ---   

Now, let’s set up a `budget`. On the left-hand side, click on `Budgets`, and here you can **"Create a budget"** that will alert you when you reach specific spending thresholds. We’ll start by creating a Zero-Spend Budget. This budget will send an alert as soon as you spend even one cent. Name this budget My Zero-Spend Budget, enter your email (e.g., stefan@example.com), and create the budget. This way, you’ll receive an email notification if any charges occur.

![](/img/04/04.png)

![](/img/04/05.png)

You can also set up a Monthly Cost Budget. For example, set a budget of `$`10 per month. This means you don’t want to spend more than `$`10 each month during this course. Enter your email again (e.g., stefan@example.com). Although you should not incur any charges if you follow the course carefully, setting up this budget is a precautionary measure.

![](/img/04/06.png)

![](/img/04/07.png)

For the `$`10 budget, you’ll receive alerts when your actual spending reaches 85% of the budget, 100% of the budget, and when your forecasted spending is expected to reach 100%. This provides multiple layers of notification to help you manage your costs effectively.

In my case, the zero-spend budget has already been exceeded because I’ve incurred some costs this month, so I received an email immediately.

By setting up these budgets, exploring the free tier usage, and reviewing your billing breakdown, you’ll be equipped to handle any costing or billing issues that arise during this course. These are essential skills when working with AWS.

#### EC2 - Basics

In this section, we will create our first website on AWS using EC2.

* EC2 is one of the most popular of AWS’ offering
* EC2 = Elastic Compute Cloud = Infrastructure as a Service
* It mainly consists in the capability of : • Renting virtual machines (EC2)
  * Storing data on virtual drives (EBS)
  * Distributing load across machines (ELB)
* Scaling the services using an auto-scaling group (ASG)
* Knowing EC2 is fundamental to understand how the Cloud works

What is Amazon EC2? EC2 stands for Elastic Compute Cloud, and it’s one of the most popular AWS offerings, widely used across various industries. EC2 provides Infrastructure as a Service (IaaS) on AWS, allowing you to rent virtual machines, known as EC2 instances.

EC2 is not just one service—it's composed of several components at a high level. You can rent virtual machines (EC2 instances), store data on virtual drives (EBS volumes), distribute load across machines using an Elastic Load Balancer, and scale services with an Auto Scaling Group (ASG). Don't worry, we'll cover all of these in depth during this course. Understanding how to use EC2 is fundamental to grasping how the cloud works because, as I mentioned before, the cloud enables you to rent compute resources on demand. EC2 is a prime example of this.


**EC2 sizing & configuration options**

* Operating System (OS): Linux, Windows or Mac OS • How much compute power & cores (CPU)
* How much random-access memory (RAM)
* How much storage space:
   * Network-attached (EBS & EFS) • hardware (EC2 Instance Store)
   * Network card: speed of the card, Public IP address
* Firewall rules: security group
* Bootstrap script (configure at first launch): EC2 User Data

So, what can we choose for our instances—our virtual servers that we rent from AWS? What operating system can we choose for our EC2 instances? There are three options: Linux, which is the most popular, Windows, and even macOS. You also need to choose how much compute power and how many cores (CPUs) you want for this virtual machine, how much random access memory (RAM), and how much storage space.

For example, do you want storage that’s attached through the network (we’ll cover this with EBS or EFS), or do you want hardware-attached storage? In the latter case, it will be an EC2 instance store. We’ll also have an entire section on storage, so don’t worry about that now. Finally, you’ll need to decide what type of network you want attached to your EC2 instance. Do you want a fast network card? What kind of public IP do you want? Additionally, you’ll need to manage the firewall rules for your EC2 instance, which is handled by the security group. Lastly, there’s the bootstrap script to configure the instance at first launch, called the EC2 user data.

So, we have lots and lots of options. As you’ll see in the hands-on exercises, there are even more options at other certification levels that you need to know about for EC2 instances. But at its core, what you need to remember is that you can choose nearly any configuration for your virtual machine and rent it from AWS. That’s the power of the cloud—you can do this in the blink of an eye, really.


**EC2 User Data**

* It is possible to bootstrap our instances using an `EC2 User data` script. 
* `bootstrapping` means launching commands when a machine starts
* That script is `only run once` at the instance first start
* EC2 user data is used to automate boot tasks such as: • Installing updates
  * Installing software
  * Downloading common files from the internet
  * Anything you can think of
* The EC2 User Data Script runs with the root user

It’s possible to bootstrap our instances using the EC2 user data script. What does bootstrapping mean? Bootstrapping means launching commands when the machine starts. This script only runs once, at the first startup, and then it will never run again. The EC2 user data has a very specific purpose: to automate boot tasks, hence the name bootstrapping.

So, what tasks might you want to automate when you boot your instance? You might want to install updates, install software, download common files from the internet, or perform any other tasks you can think of. The possibilities are endless. However, keep in mind that the more you add to your user data script, the more tasks your instance will have to perform at boot time. Simple, right? By the way, the EC2 user data script runs as the root user, so any command you include will have sudo rights.

**EC2 Instance Types: example**

![](/img/04/08.png)

#### Create EC2 Instance with EC2 UserData to have a WebSite

**Hands-On: Launching an EC2 Instance running Linux**

• We’ll be launching our first virtual server using the AWS Console  
• We’ll get a first high-level approach to the various parameters  
• We’ll see that our web server is launched using EC2 user data   
• We’ll learn how to start / stop / terminate our instance.  

In this lecture, we are going to launch our first EC2 instance running Amazon Linux. For this, we'll be launching our first EC2 instance, which is a virtual server, using the console. We'll take a high-level look at the various parameters available when launching an EC2 instance. You'll see there are many options, but we'll focus on the most important ones. Then, we'll launch a web server directly on the EC2 instance using a piece of code called user data. Finally, we'll learn how to start, stop, and terminate our instance. So, let's get started and launch our first EC2 instance.

To begin, go to the EC2 console, click on **Instances**, and then click on **Launch Instances**. 

![](/img/04/09.png)

From there, you'll be able to launch your first EC2 instance. The first step is to add a name and tags. The name will be MyFirstInstance, which will serve as the name tag. If you want to add additional tags to categorize your instance differently, you can do so, but for now, using just the name MyFirstInstance is sufficient.

Next, you need to choose a base image for your EC2 instance, which is the operating system of your instance. There is a full catalog you can search through, but we'll use one from the Quick Start section, which is very helpful. We’ll be using Amazon Linux, provided by AWS. Specifically, we'll choose the Amazon Linux 2 AMI, which is free tier eligible, so we’ll leave it as is. This gives us an Amazon Linux 2 instance with a 64-bit x86 architecture. We’ll leave everything else as default for now. In later sections, we’ll cover how to create your own AMIs and find them in this catalog, but for now, we'll stick with the ones provided by AWS in the Quick Start.

![](/img/04/10.png)


Next, we need to choose an **instance type**.   
Instance types differ based on the number of CPUs, the amount of memory, and the cost. Right now, I have a T2 Micro selected, which is free tier eligible, meaning it will be free to run for an entire month if left running continuously. This is what we’ll use. You can scroll through the list to see other instance types. For example, T1 Micro is also free tier eligible but is an older generation. There are many instance types available, some free tier eligible, some not. By default, the free tier eligible instance is T2 Micro, which we’ll use frequently. If you want to compare instance types, you can click on the link provided to see details such as memory and other specs. For now, we'll stick with T2 Micro.

Next, you need a **key pair to log** into your instance.  
This is necessary if you use the SSH utility to access your instance, which we will do in this course. Therefore, we need to create a key pair. As you can see, there’s no key pair selected by default. We could proceed without one, but for now, we won’t. Let's go ahead and `create a new key pair` named **EC2Tutorial**. 

![](/img/04/11.png)

Choose the RSA key type, which is encrypted, and select the .PEM format if you are using Mac, Linux, or Windows 10. If you are using an older version of Windows, like Windows 7 or Windows 8, you can choose the PPK format, which is used with PuTTY, the SSH client for older Windows versions. So, remember: for anything other than Windows 7 or 8, choose .PEM; otherwise, choose PPK. Once you’ve made your selection, create the key pair, and it will be downloaded automatically. 

![](/img/04/12.png)

Now, it should be selected in the console.

Next, we’ll configure the **network settings**.  
For now, we won’t change anything. Our instance will get a public IP, and we need to connect to it. A `security group` will be attached to our instance, which will control the traffic to and from the instance, and therefore we can add rules. The first security group created will be called `LaunchWizard1`, created directly by the console, and we can define multiple rules. The first rule is to allow `SSH traffic` from anywhere, so we’ll leave it as is. This will create a rule in our security group to allow SSH traffic. We also want to allow `HTTP traffic` from the internet, so we’ll check that box as well since we’ll be launching a web server on our EC2 instance. We won’t be using HTTPS for now, so we don’t need to check that box.

![](/img/04/13.png)

Now, let's configure the **storage**.  
We have an 8 GB GP2 root volume, and we'll leave it as is because the free tier provides up to 30 GB of EBS general-purpose SSD storage. This setup is sufficient, and we only need one volume. If you go into the `advanced` settings, you can configure more options, but one important thing to note is the `Delete on Termination` setting. By default, it is enabled, which means that when we terminate our EC2 instance, the volume will also be deleted. We’ll leave everything as is and return to the simple mode.

![](/img/04/14.png)

Finally, we reach the **Advanced details** section,   
where it gets interesting. We’ll skip the Spot option and the IAM instance profile for now. Don’t worry, we’ll cover them when needed. 

Scroll down to the bottom where you’ll find the User **Data section**.  
User data allows us to pass a script—some commands—to our EC2 instance that will execute on the first launch and only on the first launch. This is where we’ll input the commands we want to run during the initial boot.

```sh
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

You copy this entirely—every part of it—and then paste it here. By pasting everything, this script will be executed when the instance is first started, and only once, during the entire lifecycle of the instance. What it's going to do is update a few things, install the HTTPD web server on the machine, and then write an HTML file that will serve as our web server.

You don't need to know how to code or understand these commands, as this is provided to illustrate a few points in this lecture. Finally, to summarize, we want to start one instance. This is great, and we can review everything we have here. It all looks good, we are very happy. As you can see, in the free tier, we get a full year of 750 hours of T2 micro, which allows it to run for one month, every month. If you don't have a T2 micro in your region, then it will be a T3 micro, okay? Additionally, we get 30 gigabytes of EBS storage, and so on. So, let's launch this instance.

![](/img/04/15.png)

The instance is now being launched. Let's go to "View All Instances," `refresh`, and now my instance is in a pending state. 

It will take about 10 to 15 seconds for the instance to come up, and this is the whole power of the cloud. Thanks to the cloud, I can create an instance—or even 100 of them—very quickly, in less than 10 seconds, without owning a single server. This is extremely powerful, and we've just scratched the surface of the cloud's capabilities. Obviously, since the course is just getting started, you can get a sense of the advantages and speed the cloud offers.

Now, as you can see, my instance is running, and I want to show you a few things, okay? 

The first thing is that the instance name is "myfirstinstance," and there's an **instance ID**, which is a unique identifier for my instance. There is a **public IPv4 address**, which we'll use to access our EC2 instance, and there is also a **private IPv4 address**, which is used to access that instance internally on the AWS network, remaining private.

The instance is running, and we have some information about the **hostname**, **private DNS**, and the **instance type**, which is T2 micro. Additionally, if you scroll down, you'll see the **AMI** we're using, which is Amazon Linux 2, and the **key pair** we're using, named "EC2 tutorial," okay? You can take a look at a few details here.

![](/img/04/16.png)

We also have more information on security. The security group was created by Launch Wizard 1 with inbound rules, such as port 22 being accessible from everywhere and port 80 also being accessible from everywhere. You should have something similar; if not, start over because you probably missed a step. There's also an outbound rule allowing all communication outwards, which enables the instance to access the Internet.
![](/img/04/17.png)

For storage, we saw that we created one volume of 8 gigabytes, so we're good to go. 

![](/img/04/18.png)

Now, let's take a look at the web server running on my instance. To do this, And for this you go on public IPv4 address, you copy this, copy it, or click on "Open Address," And as you can see, it doesn't work. Or if you click on it, copy and then paste it, you press Enter, it's going to work.

![](/img/04/19.png)

So, it depends on the web browsers you have and so on, okay? But the reason it doesn't work here is that in the URL, you need to make sure that you're using the HTTP protocol. So, HTTP colon slash slash and then the IP. Because if you use HTTPS, this is not going to work, it's going to give you an infinite loading screen, which is happening right now. So, please make sure to use HTTP colon slash slash and then the IP address, and you're going to get this screen.

And in programming, when you do something for the first time, you usually say Hello World.. So, this web server is telling Hello World. from this IP right here, which is not the public IP. This IP right here, **172-31-24-169**, actually corresponds to the private IP or address. So, this is something that I programmed myself. So, we use the public IP address to access it, but we have the private IP address in here, and we have the Hello World.. And if you go too fast, you're going to get no messages. So, if you go too fast, just wait five minutes, get back to it, refresh this page, and you'll see it.

--

Okay, so, cool, we have a web server running, this is great. Now, let's explore a few options. So, we have an EC2 instance and it's running, but if we don't need it, we can go to instance state and then click on `stop instance`. And in the cloud, you can start and stop instances just as you wish. 

![](/img/04/20.png)

And why would you stop an instance? Well, the longer you leave it running, the more you're going to pay, of course. But if you decide to stop an instance, then AWS will not bill you for it. The instance state is kept because you have a volume attached to it, but at least you're not paying for it. So, you can see right now, well, the instance is in a stopping state. And if we try to refresh this page, it's going to, of course, it's not going to work because, well, we don't have the server running anymore. So, you can see, it's just like infinite loading experience.

--

Okay, so my instance is now stopped. And if I wanted to, actually, I could get rid of it. And in the cloud, it's very common to start instances and then get rid of them, just to try it out. Because this is the cloud and we can do whatever we want. So, we can do instance state and then terminate instance. 

![](/img/04/21.png)

If we do so, we're going to get a warning message. And don't click on terminate because I want to keep this instance with me, okay? But this is how we would get rid of it. So, I'll cancel this. And what I'm going to do now is I'm going to start my instance again. So, I'm going to do instance state and then start instance. And now, as you can see, the state is ending, so it is getting started. And I just wait for it to be started in a green state. And I will show you something very interesting.

Okay, so my instance is now running. And if I go here and stop the refresh and try again to refresh, as you can see, it still goes into an infinite loop. Well, you may say, well, the server is running so fast. So, why is it not displaying the message now? It is displaying here, but like from the old one, of course. So, here, the IP starts with 54, right? But here, if you click on here, now the public IP starts with 3.250. So, **the public IP actually has changed**. So, if you stop an instance and then you start it later on, then AWS will maybe change its public IP before. So, therefore, you need to copy the new IP before, make sure to use HTTP, and voila, we have access back to our distro instance. But one thing that has not changed is the private IP before. The private IP will always stay the same, but the public IP before may change, okay?

Well, so let's enter this in now. We've seen quite a lot of things. We've launched our first EC2 instance, which is very exciting, our first web server in the cloud. We had a look at some of the power of the cloud, which is using some API calls to stop an instance, start an instance, and so on. So, I hope you liked it, and I will see you in the next lecture.

#### EC2 Instance Types Basics

**EC2 InstanceTypes - Overview**

• You can use different types of EC2 instances that are optimised for different use cases (https://aws.amazon.com/ec2/instance-types/)
• AWS has the following naming convention:

![](/img/04/27.png)

Now let's talk about EC2 instance types. So there are different types of EC2 instances that you can use for different use cases, and they have different types of optimization. And let's go check out this link, and we'll see we have, for now, seven different types of EC2 instances. So this website on the AWS website is what we're interested in. And as we can see, we have different types of instances with general purpose, compute-optimized, memory-optimized, and so on. And so for each type of instance, we have different families. And so as we can see, this website is going to be the reference for us to look at EC2 instance types and know their cost and know their specificity.

What I'm going to do, though, is just walk you through a high-level overview of how they work in AWS. AWS will have the following naming convention. For example, we'll be talking about an M5.2xlarge type of instance. What does that mean? Well, M is going to be called the instance class. And this is going to be, for example, in this case, a general purpose type of instance. Five is the generation of the instance. So as AWS improves the hardware over time, it will release a new generation of hardware. And so after M5, if they improve the M type of instance class, then we'll go to M6. And then finally, the 2xlarge represents the size within the instance class. So it starts as small, and then large, and then 2xlarge, 4xlarge, and so on. So it represents the size of the instance. And the more the size, the more the memory, the more the CPU you're going to have on your instance.

So from an exam perspective, what do you need to know? Well, we'll talk about a few different types of instance types. 

**EC2 Instance Types – General Purpose**

* Great for a diversity of workloads such as web servers or code repositories
* Balance between: • Compute
  * Memory
  * Networking
* In the course, we will be using the t2.micro which is a General Purpose EC2 instance

![](/img/04/22.png)

So you have general purpose. And these are great for a diversity of workloads, such as web servers or code repositories. They will have a good balance between compute, memory, networking. And so in this course, we'll be using general purpose instances. We'll be using the T2 micro, which is the free-tier general purpose type of instance. On the website that I just showed you, you will see all the different types of instances that are general purpose. And this is going to evolve over time, so I won't update the slide. But you can always refer back to the AWS website to check what the instances are in the general purpose type of family.

**EC2 Instance Types – Compute Optimized**

• Great for compute-intensive tasks that require high performance processors:
• Batch processing workloads
• Media transcoding
• High performance web servers
• High performance computing (HPC)
• Scientific modeling & machine learning
• Dedicated gaming servers

![](/img/04/23.png)

Then we have compute optimized. And these instances are great and optimized for compute-intensive tasks. So what requires a high-level processor? Well, for example, if you're batch processing some data, if you're doing media transcoding, if you need high-performance web servers, if you're doing high-performance computing, or HPC, if you're doing machine learning, or if you have a dedicated gaming server. So all these things are tasks that require a very good CPU, a very good compute side, and so EC2 instances do have this kind of particularity. And for now, all the compute-optimized instances in EC2 are of the C name, so C5, C6, and so on.


**EC2 Instance Types – Memory Optimized** 

• Fast performance for workloads that process large data sets in memory
• Use cases:
• High performance, relational/non-relational databases
• Distributed web scale cache stores
• In-memory databases optimized for BI (business intelligence)
• Applications performing real-time processing of big unstructured data

![](/img/04/24.png)

Next, we have some EC2 instances that are memory-optimized. And they're going to have really fast performance for the type of workloads that will process large datasets in memory. So memory means RAM. And so the use cases are this is going to be high-performance for relational or non-relational databases. They're mostly going to be in-memory databases. Distributed web-scale cache stores, so for ElastiCache, for example. In-memory databases that are optimized for business intelligence, or BI. And applications performing real-time processing of big unstructured data. So in terms of the names for the memory-optimized instances, there's going to be the R series, because R stands for RAM. But there's also going to be X1, high-memory, and Z1. Again, don't remember the name of the instances, but it's going to go at a high level.

**EC2 InstanceTypes – Storage Optimized**

• Great for storage-intensive tasks that require high, sequential read and write access to large data sets on local storage
• Use cases:
• High frequency online transaction processing (OLTP) systems
• Relational & NoSQL databases
• Cache for in-memory databases (for example, Redis)
• Data warehousing applications
• Distributed file systems

![](/img/04/25.png)

Okay, and finally, we'll have storage-optimized instances. They're great when you are accessing a lot of datasets on the local storage. And so the use cases for storage-optimized instances are going to be high-frequency online transaction processing, so OLTP systems, relational and NoSQL databases, and we'll see those in detail when we get to the database sections. Cache for in-memory databases, for example, Redis. Data warehousing applications. Distributed file systems. And the storage-optimized instances in AWS will start with an I, a D, or H1. Okay, but again, you don't have to remember this. I'm just giving you examples.

**EC2 Instance Types: example**

![](/img/04/26.png)

Great website: https://instances.vantage.sh

So what does it mean? Let's compare the two instance types. So for example, for T2 micro, we have one vCPU and one gigabyte of memory. And if you look, for example, at the R5-16XLarge, we have 16 vCPUs and 512 gigabytes of memory. So we can see there's a lot more emphasis on the memory. If we compare it, for example, to a C5-24XLarge, we can see we have 96 vCPUs and 192 gigabytes of memory. So less memory, more CPU, and so on. Different network performance, different EBS bandwidth, and so on. So just to give you a point of comparison.

And because we're using T2 micro in this course, it is part of the AWS free tier, so we get up to 750 hours per month of T2 micro. And if you wanted a website to compare all the EC2 instances together, there's one that I really like. It's called ec2instances.info (https://instances.vantage.sh/), and I'll show it to you right now. So I am on the ec2instances.info website, and as we can see, we have a list of all the instances available in AWS. So really a lot. We also get some information around the Linux on-demand costs, the Linux reserved costs, and so on. So some cost information. We get information around the memory, the number of CPUs. We can order by name. We can search it. So it's quite handy, and I really like this website. And if you go and use AWS, you probably will use this website as well.

So that's it for this lecture. I hope you liked it, and I will see you in the next lecture. Let's talk about these firewalls around our EC2 instances. So we briefly configured one in the previous lecture, but security groups, yet again, are going to be fundamental.


#### Security Groups & Classic Ports Overview

**Introduction to Security Groups**

* Security Groups are the fundamental of network security in AWS
* They control how traffic is allowed into or out of our EC2 Instances.

![](/img/04/28.png)

* Security groups only contain `Allow` rules
* Security groups rules can reference by IP or by security group

Let's talk about these firewalls around our EC2 instances. We briefly configured one in the previous lecture, but security groups, yet again, are going to be fundamental to doing network security in the AWS cloud. They will control how the traffic is allowed into and out of your EC2 instances.

Security groups are going to be very easy. They only contain allowed rules, so we can say what is allowed to go in and to go out. Security groups can have rules that reference either by IP addresses, so where your computer is from, or by other security groups. As we'll see, security groups can reference each other.

Here's a second example. We are on our computer, so we are on the public Internet, and we're trying to access our EC2 instance from our computer. We are going to create a security group around our EC2 instance, that is, the firewall that is around it, and then this security group is going to have rules. These rules are going to say whether or not some inbound traffic, so from the outside into the EC2 instance, is allowed, and also if the EC2 instance can perform some outbound traffic, so to talk from where it is into the Internet.

**Security Groups - Deeper Dive**

* Security groups are acting as a “firewall” on EC2 instances
* They regulate:
  * Access to Ports
  * Authorised IP ranges – IPv4 and IPv6
  * Control of inbound network (from other to the instance)
  * Control of outbound network (from the instance to other)

![](/img/04/29.png)

Now, let's do a deeper dive. Security groups are a firewall on our EC2 instances, and they're going to regulate access to ports. They're going to see the authorized IP ranges, whether it be on IPv4 or IPv6—these are the two kinds of IP on the Internet. This is going to control the inbound network, so from the outside to the instance, and the outbound network from the instance to the outside.

When we look at the security group rules, they will look just like this. They will be the type, the protocol (e.g., TCP), the ports allowing it (where the traffic can go through on the instance), and the source, which represents an IP address range. "0.0.0.0/0" means everything, and a specific IP address would mean just one IP.


**Security - Groups Diagram**

![](/img/04/30.png)

Now, let's look at the diagram, right? So we have our EC2 instance, and it has one security group attached to it that has inbound rules and outbound rules. I've separated them onto this diagram. So our computer is going to be authorized on, say, port 22, so the traffic can go through from our computer to the EC2 instance. But someone else's computer that's not using my IP address, because they don't live where I live, if they try to access our EC2 instance, they will not get through it because the firewall is going to block it, and it will be a timeout.

Then for the outbound rules, by default, our EC2 instance for any security group is going to be by default allowing any traffic out of it. So our EC2 instance, if it tries to access a website and initiate the connection, it is going to be allowed by the security group. This is the basics of how the firewall works.

**Security Groups - Good to know**

* Can be attached to multiple instances
* Locked down to a region / VPC combination
* Does live “outside” the EC2 – if traffic is blocked the EC2 instance won’t see it
* `It’s good to maintain one separate security group for SSH access`
* If your application is not accessible (time out), then it’s a security group issue
* If your application gives a “connection refused“ error, then it’s an application error or it’s not launched
* All inbound traffic is `blocked` by default
* All outbound traffic is `authorised` by default


Now, what do you need to know with security groups? Well, they can be attached to multiple instances. There's not a one-to-one relationship between security groups and instances, and actually, an instance can have multiple security groups too. Security groups are locked down to a region/VPC combination. So if you switch to another region, you have to create a new security group, or if you create another VPC (and those VPCs are in a lecture), well, you have to recreate security groups.

The security groups live outside the EC2, so as I said, if the traffic is blocked, the EC2 instance won't even see it. It's not like an application running on EC2; it's really a firewall outside your EC2 instance.

To be honest, and that's just some advice from developer to developer, it's good to maintain one separate security group just for SSH access. Usually, SSH access is the most complicated thing, and you really want to make sure that one is done correctly, so I usually separate my security group for SSH access separately.

If your application is not accessible and times out (as we saw in the last lecture), then it is a security group issue. If you try to connect to any port, and your computer hangs, waits, and blinks, that's probably a security group issue. But if you receive a connection refused error—if you actually get a response saying "connection refused"—then the security group actually works, the traffic went through, but the application was errored, or it wasn't launched, or something like this. So this is what you would get if you receive a connection refused.

By default, all inbound traffic is blocked, and all outbound traffic is authorized. 


**Referencing other security groups Diagram**

![](/img/04/31.png)

Now, there is a small advanced feature that I really, really like, and I think it's perfect if you start using load balancers (we'll see this in the next lecture as well), which is how to reference security groups from other security groups.

So let me explain this. We have an EC2 instance, and it has a security group that I call group number one. The inbound rules are basically saying, "I'm authorizing security group number one inbound, and security group number two." So why would we even do this? Well, if you launch another EC2 instance, and it has security group two attached to it, by using the security group from the rule that we just set up, we basically allow our EC2 instance to connect straight through the port we decided onto our first EC2 instance.

Similarly, if we have another EC2 instance with a security group one attached, we've also authorized this one to communicate straight back to our instances. And so regardless of the IP of our EC2 instances, because they have the right security group attached to them, they're able to communicate straight through to other instances. And that's awesome because it doesn't make you think about IPs all the time.

If you have another EC2 instance with security group three attached to it, well, because group number three wasn't authorized in the inbound rules of security group number one, it's being denied, and things won't work. So that's a bit of an advanced feature, but we'll see it when we build the instances. It's quite a common pattern, and I just want you to know about it. Just remember this diagram, and by now you should be really, really good at security groups and understand them correctly.

**Classic Ports to know**

* 22 = SSH (Secure Shell) - log into a Linux instance
* 21 = FTP (File Transfer Protocol) – upload files into a file share
* 22 = SFTP (Secure File Transfer Protocol) – upload files using SSH
* 80 = HTTP – access unsecured websites
* 443 = HTTPS – access secured websites
* 3389 = RDP (Remote Desktop Protocol) – log into a Windows instance

Now, going into the example, what ports do we need to know? Well, we need to know something called SSH, or secure shell, and we're going to see this in the very next lecture. This is port 22, and it allows you to log into an EC2 instance on Linux.

We have port 21 for FTP, or file transfer protocol, which is used to upload files into a file server. And we have SFTP, which also uses port 22. Why? Well, because we're going to upload files, but this time using SSH, as it's going to be a secure file transfer protocol.

Then we have port 80 for HTTP, and we've been using it in the previous lecture. This is to access unsecured websites, and you see this whenever you go on the Internet and enter "http://” followed by the address of the website. You've also seen most likely more like this using HTTPS, which is to access secure websites, which are the standard nowadays. For HTTPS, it is port 443.

Finally, the last port you need to remember is 3389 for RDP, or remote desktop protocol, which is the port used to log into a Windows instance. So, 22 is SSH for a Linux instance, but 3389 is RDP for a Windows instance.

Now, this is all the theory about security groups. I will see you in the next lecture for some practice. So, we've launched our EC2 instance, and now let's have a look at security groups.

#### Security Groups Hands On

So we've launched our EC2 instance, and now let's have a look at security groups. We have a short idea of security groups by just clicking on "Security" in here, and we get an overview of the security groups attached to our instance, as well as the inbound rules and the outbound rules. But what I will do is access the more complete page of security groups from the left-hand side menu. So under "Network and Security," you click on "Security Group."

We can see so far that we have two security groups in our console: the default security group that is created by default, as well as the launch wizard one, which is the first security group that was created when we created our EC2 instance. A security group has an ID, just like an EC2 instance has an ID. Then we can check the inbound rules. 

![](/img/04/34.png)

The inbound rules are the rules that allow connectivity from the outside into the EC2 instance.

As we can see, we have two inbound rules in here. The first one is of type SSH, which allows port 22 in our instance. Let me just click on "Edit inbound rules" to see better. The first one is SSH on port 22 from anywhere. So 0.0.0.0/0 means anywhere. The second one is HTTP on port 80, again, from anywhere. This rule right here is what allowed us to access our web server.

![](/img/04/35.png)

 If you go back to the **EC2 console**, go to our instance, and use this `IPv4 address` to open it as an HTTP website, this worked thanks to this rule on `port 80`.

Let's verify this. If we delete this rule on `port 80` and save the rules, as you can see now, we only have `port 22`. If I go back to this and refresh my page, now, as you can see, there's an infinite loading screen at the top of my screen, which shows that I no longer have access to my EC2 instance.

**Here is a very important tip for you**: Anytime you see a timeout—okay, this is a timeout because it keeps on trying to connect but doesn't succeed and then eventually fails, causing a timeout—if you see a timeout when trying to establish any kind of connection into your EC2 instances, whether you are trying to SSH into it and get a timeout, or doing an HTTP query and get a timeout, or anything else, this is 100% the cause of an EC2 security group issue. In that case, go to your security group rules and make sure they are correct, because if they're not, you will get a timeout.

To fix this, we can add that rule back. We will add HTTP, which automatically allows port 80 in here, and select "Anywhere" for IPv4. Save the rule, and now it's done. If I go back to my page and refresh, as you can see, it is now fully working. This inbound rule really did the trick.

But we could add any sort of inbound rule. We could define the port or the port range that we want to allow. For example, we could set any port we want, such as 443, which is HTTPS, or choose directly from the dropdown here as a shortcut for the type of protocol you want. For example, HTTPS is automatically set to port 443. Then you can define where you want to allow access from. You have different CIDR blocks—though we don't use them right now—or security groups, or prefix lists, but we'll get to see them later on in this course.

![](/img/04/37.png)

For now, just know that you can have either a custom CIDR, "Anywhere," which is this block, or you can select "My IP" to only allow access from your IP. But be wary that if your IP changes, you will get a timeout and will not be able to access your EC2 instance.

Finally, one last bit of information: We can look at the outbound rules. We allow all traffic on IPv4 to anywhere, which gives our EC2 instance full Internet connectivity. Something else to note: We have two security groups here, "default" and "launch-wizard-1." An EC2 instance can have multiple security groups attached to it. You can attach one, two, three, or even five security groups, and the rules will just add on to each other.

Also, this security group we created earlier, such as "launch-wizard-1," can be attached to other EC2 instances. You can attach as many security groups as you want, as well as as many EC2 instances as you want to one security group.


#### SSH Overview

**SSH SummaryTable**

![](/img/04/32.png)


**Which Lectures to watch**
* Mac / Linux:
  * SSH on Mac/Linux lecture
* Windows:
  * Putty Lecture
  * If Windows 10: SSH on Windows 10 lecture
* All:
  * EC2 Instance Connect lecture

**SSH troubleshooting**

* Students have the most problems with SSH
* If things don’t work...
  1. Re-watch the lecture.You may have missed something
  2. Read the troubleshooting guide
  3. Try EC2 Instance Connect
* If one method works (SSH, Putty or EC2 Instance Connect) you’re good
* If no method works, that’s okay, the course won’t use SSH much

**How to SSH into your EC2 Instance** `Linux / Mac OS X`

• We’ll learn how to SSH into your EC2 instance using Linux / Mac
• SSH is one of the most important function. It allows you to control a remote machine, all using the command line.

![](/img/04/38.png)

• We will see how we can configure OpenSSH ~/.ssh/config to facilitate the SSH into our EC2 instances

--

Right, so now we're going to SSH into our EC2 instance using our Linux or Mac computer. And you may say, what the hell is SSH? What are you talking about, Stéphane? Well, SSH is one of the most important functions when you deal with Amazon Cloud. It basically allows you to control a remote machine or server all using your terminal or your command line.

So how does that look like with a diagram? Well, we have our EC2 machine, and we launched Amazon Linux 2 on it, and our machine has a public IP. Now we want to access that machine. For this, I don't know if you remember, but we have a security group, and on it, we allow the port 22 of SSH. So what's going to happen is that our computer (my laptop for me, or whatever you're using) will access the EC2 machine over the web through that port 22. Basically, our command line interface is going to be just as if we were inside that machine.

So let's get started. Okay, we are going to SSH into our instance. Remember that PEM file we downloaded called ec2-tutorial.pem. Please make sure to remove any spaces in the filename if you have them. Even if you have a PPK file, please rename it and remove any spaces from it. So, ec2-tutorial.pem is removed for me. Then you should place it in a directory you like. For me, I took my file, pasted it, and placed it in a folder called AWS course. This is the first step to ensuring you are ready.

Next, I'm going to go to my EC2 instance overview page and find my first instance. So here we have my first instance, and we are going to SSH into it. We will open a remote terminal into it. For this, I need to get the public IPv4 address, so I can copy this, and I will use it later. 

Next, I'm going to go to my EC2 instance overview page and find my first instance. So here we have my first instance, and we are going to SSH into it. We will open a remote terminal into it. For this, I need to get the public IPv4 address, so I can copy this, and I will use it later. 

![](/img/04/39.png)

 The other thing I need to do is to look at the security of my instance. Again, if you followed along, your security groups should have a rule called port 22, which is the SSH port, allowing access from anywhere (0.0.0.0/0). If you have that rule, then you are good to go. If not, please click on the security group and add the missing rule.

 ![](/img/04/40.png)

 Next, I need to try to SSH into the instance. First, we do ssh ec2-user@, and then the IP you have. The reason we use ssh ec2-user is because the Amazon Linux 2 AMI has one user already set up for us, and that user is named ec2-user. The @ symbol indicates that we want to access that user on a specific server, and then we provide the public IP of our EC2 instance.

 ```sh
➜  ~ ssh ec2-user@54.210.241.119

The authenticity of host '54.210.241.119 (54.210.241.119)' can't be established.
ED25519 key fingerprint is SHA256:sLsKZ1jadtgMx8hz/bqG8gozD73xi4Z37gzwzSRw4jY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '54.210.241.119' (ED25519) to the list of known hosts.
ec2-user@54.210.241.119: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
 ```

 So we try this, typing ssh followed by the command. If you get a "too many authentication failures" error, it means we haven't authenticated into our EC2 instance yet. That makes sense because we haven't specified the key that we downloaded before. You might get another kind of error, but right now, this is the one I get.

To resolve this, we need to reference the PEM file we just downloaded (ec2-tutorial.pem) in our command. Make sure again there is no space in the filename. Also, ensure your terminal is exactly where your file is located. If I run ls right now to list the files in my folder—I'm sorry if this is too advanced for some, but I need to cover all the bases—you should see ec2-tutorial.pem. That's because I placed my command line in the correct directory on my computer.

For example, if I wasn't in the correct directory, and I moved one level up by typing cd .. and then ran ls, of course, I wouldn't see ec2-tutorial.pem. To find where you are, you can use the pwd command, which will show your current directory. For instance, if you're in /Users/StephaneMarrec and know that you placed your folder aws-course within your home directory, you can use ls or ll to confirm that the folder exists. Once confirmed, you can navigate to it by typing cd aws-course.

Now, if I run pwd, I see that I'm in the correct directory. Running ls confirms that ec2-tutorial.pem is in the folder. The reason I do this is that in the next command, the ssh -i command, you need to specify the ec2-tutorial.pem file, and this won't work if you're not in the correct directory. So please make sure to navigate to the correct directory.


 ```sh
 ➜  aws-course ls -la
total 8
drwxr-xr-x@  3 alex  staff    96 Aug 16 18:50 .
drwx------@ 43 alex  staff  1376 Aug 16 18:51 ..
-rw-r--r--@  1 alex  staff  1674 Aug 16 09:08 ec2-tutorial.pem
➜  aws-course pwd
/Users/alex/Desktop/aws-course
➜  aws-course ssh -i ec2-tutorial.pem ec2-user@54.210.241.119
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'ec2-tutorial.pem' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "ec2-tutorial.pem": bad permissions
ec2-user@54.210.241.119: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
```

If you're missing a bit of Linux knowledge here, try looking it up online, but what I've shown you should suffice. Then type ssh -i ec2-tutorial.pem ec2-user@, followed by the public IP of your instance. After pressing enter, you might encounter an "unprotected private key file" error, which indicates that you need to change the permissions for the file. To fix this, run the command chmod 0400 ec2-tutorial.pem.

```sh
➜  aws-course ls
ec2-tutorial.pem
➜  aws-course chmod 0400 ec2-tutorial.pem
➜  aws-course ssh -i ec2-tutorial.pem ec2-user@54.210.241.119
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-172-31-24-169 ~]$ 

```

Let's try a few commands. For example, if you type whoami, it should return ec2-user. Or, you can type ping google.com, and you'll see that Google responds to your ping. I used Ctrl-C to stop the command. To exit the instance itself, you can either type exit or press Ctrl-D, which will close the connection to the EC2 instance.

If you ever want to get back into it, remember the command: ssh -i ec2-tutorial.pem ec2-user@, followed by the public IP of your instance. Also, remember that if you stop and start your instance, the public IP can change, so make sure to update that part of the command as well.

```sh
[ec2-user@ip-172-31-24-169 ~]$ whoami
ec2-user

[ec2-user@ip-172-31-24-169 ~]$ ping google.com

PING google.com (142.251.16.113) 56(84) bytes of data.
64 bytes from bl-in-f113.1e100.net (142.251.16.113): icmp_seq=1 ttl=56 time=1.84 ms
64 bytes from bl-in-f113.1e100.net (142.251.16.113): icmp_seq=2 ttl=56 time=3.58 ms
--- google.com ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 1.838/2.711/3.584/0.873 ms

[ec2-user@ip-172-31-24-169 ~]$ logout
Connection to 54.210.241.119 closed.
➜  aws-course 
```

**SSH Troubleshooting**


1) There's a connection timeout
   * This is a security group issue. Any timeout (not just for SSH) is related to security groups or a firewall. Ensure your security group looks like this and correctly assigned to your EC2 instance.


2) There's still a connection timeout issue
     * If your security group is properly configured as above, and you still have connection timeout issues, then that means a corporate firewall or a personal firewall is blocking the connection. Please use EC2 Instance Connect as described in the next lecture.


3) SSH does not work on Windows
   * If it says: `ssh command not found`, that means you have to use Putty
   * Follow again the video. If things don't work, please use EC2 Instance Connect as described in the next lecture

4) There's a connection refused
  This means the instance is reachable, but no SSH utility is running on the instance
      * Try to restart the instance
      * * If it doesn't work, terminate the instance and create a new one. Make sure you're using Amazon Linux 2

5) `Permission denied (publickey,gssapi-keyex,gssapi-with-mic)`

    This means either two things:

      * You are using the wrong security key or not using a security key. Please look at your EC2 instance configuration to make sure you have assigned the correct key to it.

      * You are using the wrong user. Make sure you have started an Amazon Linux 2 EC2 instance, and make sure you're using the user ec2-user. This is something you specify when doing ec2-user@<public-ip> (ex: ec2-user@35.180.242.162) in your SSH command or your Putty configuration

6) Nothing is working - "aaaahhhhhh"  
    Don't panic. Use EC2 Instance Connect from the next lecture. Make sure you started an Amazon Linux 2 and you will be able to follow along with the tutorial :)

7) I was able to connect yesterday, but today I can't  
    This is probably because you have stopped your EC2 instance and then started it again today. When you do so, the public IP of your EC2 instance will change. Therefore, in your command, or Putty configuration, please make sure to edit and save the new public IP.


#### EC2 Instance Connect

I want to show you an alternative to SSH that I found a lot easier, which is the EC2 Instance Connect. So for this, you click on "My First Instance," and then you click on the top where it says "Connect." You have multiple options, including the SSH Connect we saw before. The option I want to show you is the EC2 Instance Connect. This allows us to do a browser-based SSH session into our EC2 instance.

![](/img/04/41.png)

For this, we verify the public IP address, which is good. The EC2 username is provided by default, which is ec2-user, because AWS guessed that we are using Amazon Linux 2, and therefore ec2-user is the correct username. But if you wanted to, you could override it, though it doesn't work unless you enter ec2-user, so we'll leave it as is for now.

As you can see, there is no SSH key option because, well, when we connect to it, it will upload a temporary SSH key for us and establish a connection this way. So with this methodology, we don't even need to manage SSH keys, which I found lovely. You click on "Connect," 

![](/img/04/42.png)

and it's going to open a new tab, and very quickly, you are into your Amazon Linux 2 AMI, and you can start running some commands, such as whoami or ping google.com, and as you can see, everything is working.

![](/img/04/43.png)

The cool thing about it is that, well, your session is in the browser instead of using a different command line interface, such as a terminal. So you can run commands like ping google.com or do any kind of command you want, really, without using the SSH utility beforehand. But in this course, if I say "Use SSH," you have the option to use your own terminal and SSH, or to use, for example, PuTTY, or to use the SSH command on Windows. Regardless of whether you're on Windows, Linux, or Mac, you can use EC2 Instance Connect.


Now, this method is relying on SSH behind the scenes. So if I go, for example, to my instance, look at the security group, and want to edit the rules, I click on my security group in the inbound rules section, edit them, and then remove the SSH inbound rule.

![](/img/04/44.png)

![](/img/04/45.png)

![](/img/04/46.png)

After deleting it and saving the rules, I go back to my EC2 instances, close the current session, and try to establish a new EC2 Instance Connect session.

![](/img/04/48.png)

As you can see, this is not working because to connect to your instance, the first thing you need to do is open port 22. So back into my launch wizard, I can fix this. I will edit the inbound rule, add the SSH rule from "Anywhere" (IPv4), save the rule, and just in case it doesn't work for you, sometimes it's because you're using IPv6. Therefore, you need to add "Anywhere" (IPv6) as well, so you need to add these two entries for your EC2 Instance Connect to work sometimes; it depends on your setup.

So we're good to go, and now if we try to connect to the instance itself—let's try to connect here—voilà, we are into the instance. So that was a quick demo of EC2 Instance Connect. I will use it a lot in this course.

#### EC2 Instance Roles Demo

Let's practice using IAM roles for our EC2 instance. First, I'm going to connect to my EC2 instance. You can SSH or use EC2 Instance Connect if you prefer. I will use EC2 Instance Connect because it's in my web browser and a little bit simpler. So back into my instance, we have EC2 Instance Connect right here, and we are in our EC2 instance. As we can see, we are the ec2-user at the public IP of our project. So regardless of whether you're using EC2 Instance Connect, SSH through your terminal, or PuTTY, if you see this, we are at the same stage, okay?

```sh
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
Last login: Fri Aug 16 18:12:56 2024 from 18.206.107.29
[ec2-user@ip-172-31-24-169 ~]$
```

Now you can run some Linux commands. For example, ping Google by typing ping google.com, and you will get some information out of Google. Press Ctrl-C to stop the ping, or issue any other Linux command you want. You don't need to know Linux commands for the exam, but this is just a Linux terminal available to you right now in the cloud. So we'll type clear to clear the screen.

```sh
[ec2-user@ip-172-31-24-169 ~]$ aws --version
aws-cli/2.15.30 Python/3.9.16 Linux/6.1.102-108.177.amzn2023.x86_64 source/x86_64.amzn.2023 prompt/off

[ec2-user@ip-172-31-24-169 ~]$ aws iam list-users
Unable to locate credentials. You can configure credentials by running "aws configure".
```

Next, we need to run some IAM commands. The cool thing is that the Amazon Linux 2 AMI we're using right now comes with the AWS CLI pre-installed. So what we can do is start using some commands. For example, type aws iam list-users. If we do so, it says "Unable to locate credentials. You can configure credentials by running AWS Configure."

We could indeed run aws configure to configure the credentials and specify an access key ID, a secret access key, and a region name. But this is a really, really, really bad idea. 

```sh
[ec2-user@ip-172-31-24-169 ~]$ aws configure
AWS Access Key ID [None]: 
AWS Secret Access Key [None]: 
Default region name [None]: 
Default output format [None]: 
```

The reason is that if we run aws configure and enter our personal details onto this EC2 instance, then anyone else with access to our account could connect to our EC2 instance (e.g., using EC2 Instance Connect) and retrieve the values of these credentials from our instance, which is not what we want. 

![](/img/04/49.png)

This is something that's really, really bad. So as a rule of thumb, never, ever, ever enter your IAM API keys (the access key ID and the secret access key) into an EC2 instance. This is horrible. 

Instead, we should use IAM roles. If you remember, when we were in the management console under IAM, we created an IAM role. So let's go back into the roles. We had a role called demo-role-for-EC2 that had one policy attached called IAMReadOnlyAccess. We are going to attach this role to our EC2 instance to provide it with credentials.

![](/img/04/50.png)

![](/img/04/51.png)

How do we do this? First, go into the "Security" tab of your instance details. As you can see, there is no IAM role currently attached to our instance. So what we can do is go back to "Instances," click on "Actions," then "Security," and select "Modify IAM role." 

![](/img/04/52.png)

Here, choose an IAM role, so we'll select demo-role-for-EC2, and click on "Save" to attach this IAM role to our instance.

![](/img/04/53.png)

If we go back to "Security," we can now see that the IAM role attached to our instance is demo-role-for-EC2. The effect of this is that now if we run aws iam list-users and press enter, we get a response listing the users from IAM. Notice that we did not run the command aws configure; we simply attached an IAM role and ran this command, and it worked.

![](/img/04/54.png)

The effect of this is that now if we run aws iam list-users and press enter, we get a response listing the users from IAM. Notice that we did not run the command aws configure; we simply attached an IAM role and ran this command, and it worked.

```sh
[ec2-user@ip-172-31-24-169 ~]$ aws iam list-users
{
    "Users": [
        {
            "Path": "/",
            "UserName": "Alex",
            "UserId": "AIDASFIXCXAFSBSZAH6YO",
            "Arn": "arn:aws:iam::148761655307:user/Alex",
            "CreateDate": "2024-08-14T10:50:02+00:00",
            "PasswordLastUsed": "2024-08-14T11:40:06+00:00"
        },
        {
            "Path": "/",
            "UserName": "Nuria",
            "UserId": "AIDASFIXCXAF7F3AAWSRL",
            "Arn": "arn:aws:iam::148761655307:user/Nuria",
            "CreateDate": "2024-08-14T10:53:51+00:00",
            "PasswordLastUsed": "2024-08-15T09:36:30+00:00"
        }
    ]
}
[ec2-user@ip-172-31-24-169 ~]$ 
```

As proof, if we go into this role and detach the permission, `IAM` > `Roles` > `DemoRoleForEC2` so now it's gone, and run the command again, we get an "Access Denied" message. This shows that the role is truly linked to the EC2 instance, and this is how we provide AWS credentials to our EC2 instances—only through IAM roles.

```sh
[ec2-user@ip-172-31-24-169 ~]$ aws iam list-users

An error occurred (AccessDenied) when calling the ListUsers operation: User: arn:aws:sts::148761655307:assumed-role/DemoRoleForEC2/i-016edbc842e56bc9c is not authorized to perform: iam:ListUsers on resource: arn:aws:iam::148761655307:user/ because no identity-based policy allows the iam:ListUsers action
```

If we go back to IAM, reattach the policy to this role (e.g., IAMReadOnlyAccess), and then rerun the command, we may still get an "Access Denied" message initially because it can take a little time for the changes to propagate from IAM to AWS. However, if we run the command again after a short wait, we get the output we expect.

![](/img/04/55.png)

```sh
[ec2-user@ip-172-31-24-169 ~]$ aws iam list-users
{
    "Users": [
        {
            "Path": "/",
            "UserName": "Alex",
            "UserId": "AIDASFIXCXAFSBSZAH6YO",
            "Arn": "arn:aws:iam::148761655307:user/Alex",
            "CreateDate": "2024-08-14T10:50:02+00:00",
            "PasswordLastUsed": "2024-08-14T11:40:06+00:00"
        },
        {
            "Path": "/",
            "UserName": "Nuria",
            "UserId": "AIDASFIXCXAF7F3AAWSRL",
            "Arn": "arn:aws:iam::148761655307:user/Nuria",
            "CreateDate": "2024-08-14T10:53:51+00:00",
            "PasswordLastUsed": "2024-08-15T09:36:30+00:00"
        }
    ]
}
[ec2-user@ip-172-31-24-169 ~]$ 
```

So, it's very important for you to understand this: use IAM roles for your EC2 instances. I hope this hands-on exercise was helpful, and I will see you in the next lecture.


#### EC2 Instances Purchasing Options

* On-Demand Instances – short workload, predictable pricing, pay by second
* Reserved (1 & 3 years)
  * Reserved Instances – long workloads
  * Convertible Reserved Instances – long workloads with flexible instances
* Savings Plans (1 & 3 years) –commitment to an amount of usage, long workload • Spot Instances – short workloads, cheap, can lose instances (less reliable)
* Dedicated Hosts – book an entire physical server, control instance placement
* Dedicated Instances – no other customers will share your hardware
* Capacity Reservations – reserve capacity in a specific AZ for any duration

--

We've been using, so far, on-demand EC2 instances. They allow us to run instances on demand, meaning they're good for short workloads, we get predictable pricing, and we're going to pay by the second. But if you have different kinds of workloads, you can optimize your discounts and pricing by specifying it to AWS.

For example, you can use reserved instances, which offer one-year or three-year terms, and they're meant for long workloads. So, if you know you're going to run a database for a long time, then a reserved instance is great. If you want to have a flexible instance type, allowing you to change the instance type over time, then convertible reserved instances are for you. And, by the way, don't worry, I'm going to do a deep dive into all of these over time.

Next, we have savings plans. Savings plans also have one-year and three-year terms, and they're more modern because instead of committing to a specific instance type, you commit to a specific amount of usage in dollars. They're also intended for long workloads.

Spot instances, on the other hand, are meant for very short workloads. They're very, very cheap, but at any time, you can lose these instances, making them less reliable.

Dedicated hosts allow you to book an entire physical server and control instance placements, while dedicated instances ensure that no other customers will share your hardware.

Finally, capacity reservations allow you to reserve capacity in a specific Availability Zone (AZ) for any duration.


**EC2 On Demand**

* Pay for what you use:
  * Linux or Windows - billing per second, after the first minute 
  * All other operating systems - billing per hour
* Has the highest cost but no upfront payment
* No long-term commitment
* Recommended for short-term and un-interrupted workloads, where you can't predict how the application will behave
  
--

You're going to pay for what you use. This means that if you're using Linux or Windows, you will be billed per second after the first minute. For all other operating systems, you'll be billed per hour. It has the highest cost but requires no upfront payment and no long-term commitments. This makes it ideal for short-term and uninterrupted workloads where you cannot predict how the application will behave.


**EC2 Reserved Instances**

* Up to 72% discount compared to On-demand
* You reserve a specific instance attributes (Instance Type, Region,Tenancy, OS)
* Reservation Period – 1 year (+discount) or 3 years (+++discount)
* Payment Options – No Upfront (+), Par tial Upfront (++), All Upfront (+++) 
* Reserved Instance’s Scope – Regional or Zonal (reserve capacity in an AZ)
* Recommended for steady-state usage applications (think database)
* You can buy and sell in the Reserved Instance Marketplace

* Convertible Reserved Instance
  * Can change the EC2 instance type, instance family, OS, scope and tenancy 
  * Up to 66% discount

-- 

This is it, by the way. The numbers I show you can change every time, so I will not update this video every time, but it gives you an idea of what the numbers can be.

Reserved instances give you a 72% discount compared to on-demand, and you reserve specific instance attributes, such as the instance type, the region, the tenancy, and the OS. You specify a reservation period, either 1 year or 3 years, to get even more discounts, and whether or not you want to pay upfront, partially upfront, or not upfront. Paying all upfront, of course, gives you the maximum amount of discounts.

You can choose whether you want the scope to be in a specific region or zone, which means reserved capacity in a specific Availability Zone (AZ). You would use reserved instances for steady-state usage applications, such as a database. Additionally, you can buy or sell your reserved instances in a marketplace if you no longer need them.

Convertible Reserved Instances:
There is a specific kind of reserved instance called the convertible reserved instance, which allows you to change the instance type, instance family, operating system, scope, and tenancy. Because you have more flexibility, you get a baseline discount of up to 66%.

**EC2 Savings Plans**

* Get a discount based on long-term usage (up to 72% - same as RIs)
* Commit to a certain type of usage ($10/hour for 1 or 3 years)
* Usage beyond EC2 Savings Plans is billed at the On-Demand price
  
* Locked to a specific instance family & AWS region (e.g., M5 in us-east- 1)
  * Flexible across:
  * Instance Size (e.g., m5.xlarge, m5.2xlarge) • OS (e.g., Linux, Windows)
  * Tenancy (Host, Dedicated, Default)

--

Now, you have the EC2 savings plan, which allows you to get a discount based on long-term usage, similar to the 70% offered by reserved instances. However, instead of reserving an instance, you're committing to spending a certain amount, such as $10 per hour, for the next 1 to 3 years. Any usage beyond the savings plan commitment is billed at the on-demand price.

With savings plans, you're locked to a specific instance family and region. For example, you might choose an M5 instance family in US East 1. However, you're flexible across the instance size (e.g., M5XLarge, M5X2Large), the OS (e.g., Linux, Windows), and the tenancy (e.g., host, dedicated, and default).

**EC2 Spot Instances**

* Can get a discount of up to 90% compared to On-demand
* Instances that you can “lose” at any point of time if your max price is less than the current spot price
* The MOST cost-efficient instances in AWS
* Useful for workloads that are resilient to failure 
  * Batch jobs
  * Data analysis
  * Image processing
  * Any distributed workloads
  * Workloads with a flexible start and end time

* Not suitable for critical jobs or databases

--

Spot instances have the most aggressive discounts, so that's Spot instances offer up to a 90% discount compared to on-demand instances. However, they are instances you can lose at any time because you define a maximum price you're willing to pay for your spot instances, and if the spot price goes over that amount, you will lose the instance. They are the most cost-efficient instances in AWS and are very helpful if you have a workload that is resilient to failure.

Spot instances are suitable for batch jobs, data analysis, image processing, any kind of distributed workloads, or workloads that have a flexible start and end time. They are not suited for critical jobs or databases, and the exam will likely test you on this distinction.


**EC2 Dedicated Hosts**

* A physical server with EC2 instance capacity fully dedicated to your use
* Allows you address compliance requirements and use your existing server- bound software licenses (per-socket, per-core, pe—VM software licenses)
* Purchasing Options:
  * On-demand – pay per second for active Dedicated Host
  * Reserved - 1 or 3 years (No Upfront, Partial Upfront,All Upfront)
* The most expensive option
* Useful for software that have complicated licensing model (BYOL – Bring Your
Own License)
* Or for companies that have strong regulatory or compliance needs

--

Dedicated hosts provide you with an actual physical server with EC2 instance capacity fully dedicated to your use case. You might choose dedicated hosts if you have compliance requirements or need to use your existing server-bound software licenses, particularly if those licenses are billed per socket, per core, or per VM. These are the scenarios where you would need to access the physical server and get a dedicated host.

For dedicated hosts, you can choose on-demand billing, where you pay per second, or you can reserve them for one or three years. They are the most expensive option in AWS because you are reserving a physical server. The primary use cases include when you have software with a bring-your-own-license model or if your company has strong regulatory or compliance needs.

**EC2 Dedicated Instances**

* Instances run on hardware that’s dedicated to you
* May share hardware with other instances in same account
* No control over instance placement (can move hardware after Stop / Start)

-- 

We also have dedicated instances, and they are instances that run on hardware dedicated to you, which is different from the physical server. However, you may share the hardware with other instances in the same account, and you have no control over instance placement. There's a difference between dedicated instances and dedicated hosts: dedicated instances mean that you have your own instance on your own hardware, whereas with dedicated hosts, you get access to the physical server itself, giving you visibility into the lower-level hardware. In the exam, this difference is important to remember, though it typically won't trick you into confusing one with the other.

**EC2 Capacity Reservations**

* Reserve On-Demand instances capacity in a specific AZ for any duration
* You always have access to EC2 capacity when you need it
* No time commitment (create/cancel anytime), no billing discounts
* Combine with Regional Reserved Instances and Savings Plans to benefit from billing discounts
* You’re charged at On-Demand rate whether you run instances or not
* Suitable for short-term, uninterrupted workloads that needs to be in a specific AZ

-- 

Next, we have capacity reservations for EC2. You can reserve on-demand instances in a specific Availability Zone (AZ) for any duration, and then you get access to that capacity whenever you need it. There is no time commitment, so you can reserve capacity or cancel your reservation at any time, and there are no billing discounts. The only purpose is to reserve capacity. If you want to get billing discounts, you need to combine it with regional reserved instances or your savings plan. You're charged the on-demand rate whether or not you run instances. This means that your reserved capacity will be paid for, and you know for sure that if you want to launch instances, they'll be available. However, if you don't launch them, you're still going to be charged. Capacity reservations are very suitable for short-term uninterrupted workloads that need to be in a specific AZ.


**Which purchasing option is right for me?**

* **On demand**: coming and staying in resort whenever we like, we pay the full price
* **Reserved**: like planning ahead and if we plan to stay for a long time, we may get a good discount.
* **Savings Plans**: pay a certain amount per hour for certain period and stay in any room type (e.g., King, Suite, Sea View, ...)
* **Spot instances**: the hotel allows people to bid for the empty rooms and the highest bidder keeps the rooms.You can get kicked out at any time
* **Dedicated Hosts**: We book an entire building of the resort
* **Capacity Reservations**: you book a room for a period with full price even you don’t stay in it

**Price Comparison**

Example – m4.large – us-east-1

![](/img/04/56.png)

In terms of price comparison, here’s a table to give you an example at one point in time. I took an M4 Large in US East 1. The on-demand price is $0.10 per hour, but the spot price can offer up to a 61% discount. If you want to reserve your instance, you have different pricing options depending on whether you choose a 1-year or 3-year term, and whether you pay no upfront, partial upfront, or all upfront. Similarly, the EC2 savings plan offers the same discount as the reserved instance discount. For reserved convertible instances and dedicated hosts, you can get up to a 70% discount if you reserve your host. Capacity reservations are priced at the on-demand rate.

Exam Tips:
The exam will ask you to know which type of instance is the right one based on your workload. By now, you should have some good hints, and don't worry, we will practice this over time.


#### Shared Responsibility Model for EC2

![](/img/04/57.png)


#### EC2 Section – Summary

• **EC2 Instance**: AMI (OS) + Instance Size (CPU + RAM) + Storage + security groups + EC2 User Data
• **Security Groups**: Firewall attached to the EC2 instance
• **EC2 User Data**: Script launched at the first start of an instance
• **SSH**: start a terminal into our EC2 Instances (port 22)
• **EC2 Instance Role**: link to IAM roles
• **Purchasing Options**: On-Demand, Spot, Reserved (Standard + Convertible), Dedicated Host, Dedicated Instance


### EC2 Instance Storage

**What’s an EBS Volume?**

• An `EBS (Elastic Block Store) Volume` is a `network` drive you can attach to your instances while they run
• It allows your instances to persist data, even after their termination
• They can only be mounted to one instance at a time (at the CCP level)
• They are bound to a specific availability zone
• Analogy:Think of them as a “network USB stick”
• Free tier: 30 GB of free EBS storage of type General Purpose (SSD) or Magnetic per month

--

First, the most important ones are going to be EBS volumes, so let's define what they are. An EBS volume stands for Elastic Block Store. It's a network drive that you can attach to your instances while they run, and we'll be using them without even knowing it. These EBS volumes allow us to persist data even after the instance is terminated. That is the whole purpose: we can recreate an instance, mount the same EBS volume from before, and get back our data. This is very helpful.

At the CCP level, these EBS volumes can only be mounted to one instance at a time. When you create an EBS volume, it is bound to a specific availability zone. This means that you cannot have an EBS volume created in, for example, US-East-1A, attached to an instance in US-East-1B. We'll see this in the diagram in a second.

So how do you think of EBS volumes? Well, you can think of them as network USB sticks. It's a USB stick that you can take from one computer and put into another, but you actually don't physically put it into the computer; it's attached through the network. This feature gives us 30 gigabytes of free EBS storage of type general purpose SSD or magnetic per month. In this course, we'll be using GP2 or GP3 volumes.

**EBS Volume**

* It’s a network drive (i.e. not a physical drive)
  * It uses the network to communicate the instance, which means there might be a bit of latency
  * It can be detached from an EC2 instance and attached to another one quickly
* It’s locked to an Availability Zone (AZ)
  * An EBS Volume in us-east-1a cannot be attached to us-east-1b 
  * To move a volume across, you first need to snapshot it
* Have a provisioned capacity (size in GBs, and IOPS)
  * You get billed for all the provisioned capacity
  * You can increase the capacity of the drive over time

--

Now let's look at it. EBS volumes are network drives, as I said. They are not physical drives. To communicate between the instance and the EBS volume, the network will be used. Because the network is involved, there may be a bit of latency when one computer tries to reach another server.

EBS volumes, because they are network drives, can be detached from an EC2 instance and attached to another one very quickly. This makes them super handy when you want to do failovers, for example. EBS volumes are locked to a specific availability zone. As I mentioned earlier, if it's created in US-East-1A, it cannot be attached to US-East-1B. However, we'll see in this section that if we do a snapshot, we can move a volume across different availability zones.

Finally, it's a volume, so you have to provision capacity in advance. You need to specify how many gigabytes you want in advance, as well as the IOPS (IO operations per second). You're basically defining how you want your EBS volume to perform. You will be billed for that provisioned capacity, and you can increase the capacity over time if you want better performance or more size.

`EBS Volume - Example`

![](/img/04/58.png)

So what does this look like as a diagram? Well, we have US-East-1A, and we have one EC2 instance. We can attach, for example, one EBS volume to that EC2 instance. If we create another EC2 instance, an EBS volume cannot be attached to two instances simultaneously at the CCP level. Therefore, this other EC2 instance will need its own EBS volume attached to it. However, it is very possible for us to have two EBS volumes attached to one instance—think of it as two network USB sticks in one machine. That makes a lot of sense.

Now, EBS volumes are linked to an availability zone. As you can see, this entire diagram so far has been using US-East-1A. If you want to have other EBS volumes in another AZ, you would need to create them separately in that other availability zone. Just as your EC2 instances are bound to an AZ, so are the EBS volumes.

**EBS – Delete on Termination attribute**

![](/img/04/59.png)

* Controls the EBS behaviour when an EC2 instance terminates
  * By default, the root EBS volume is deleted (attribute enabled)
  * By default, any other attached EBS volume is not deleted (attribute disabled)
* This can be controlled by the AWS console / AWS CLI
* Use case: preserve root volume when instance is terminated

--

Finally, it is possible for us to create EBS volumes and leave them unattached. They don't necessarily need to be attached to an EC2 instance; they can be attached on demand, which is very powerful.

When we create EBS volumes through EC2 instances, there is a setting called the "delete on termination" attribute, and this can come up in the exam. When we create an EBS volume in the console while creating an EC2 instance, there is a second-to-last column called "delete on termination." By default, it is ticked for the root volume and not ticked for a new EBS volume. This setting controls the EBS volume's behavior when an EC2 instance is terminated.

By default, as you can see, the root EBS volume is deleted when the instance is terminated. This setting is enabled by default. Any other attached EBS volume is not deleted because the setting is disabled by default. However, as we can see in the UI, we can control whether to enable or disable "delete on termination."

A use case for this would be if you want to preserve the root volume when an instance is terminated, for example, to save some data. In that case, you can disable "delete on termination" for the root volume, and you'll be good to go. This could be a scenario presented in the exam.

#### About EBS Multi-Attach

While I say that in the previous lecture that EBS volumes cannot be attached to multiple instances, I know it is not true for io1 and io2 volume types: this is called the EBS Multi-Attach feature.

From an AWS Cloud Practitioner exam perspective this out of scope for the exam.
In order to keep the course simple and accessible, I have left out this feature from the course.

If you are curious to learn about EBS Multi-Attach, you will find it in the AWS Certified Solutions Architect Associate course, or in the [AWS documentation](https://docs.aws.amazon.com/ebs/latest/userguide/ebs-volumes-multi.html).


#### EBS Hands On

Look at the EBS volumes attached to our instance.

If you click on the Instance and then go to the Storage tab, you'll find that there is a root device and a block device on it. As you can see, we have one volume of 8 GB currently attached to our EC2 instance.

![](/img/04/60.png)

You can click on this volume, which will take you to the volumes interface in AWS. Here, you can see that, yes indeed, our volume exists, is in use, and is attached to an instance.

Now, let's explore this in more detail. To access the volumes interface, you can click on Volumes on the left-hand side. As you can see, we have one EBS volume of 8 GB. What I can do now is create a second volume. Let me create a volume. 

![](/img/04/61.png)

 I will have many options to choose from, such as GP2, GP3, and so on. I'll choose GP2 with a size of 2 GB.

![](/img/04/62.png)

Next, for the Availability Zone, I'll choose the same one where my EC2 instance is located. To find out which Availability Zone my EC2 instance is in, I'll scroll down to the Networking section, where it says Availability Zone. It indicates `us-east-1d`, 

![](/img/04/63.png)

so the volume I create will also be in `us-east-1d` because EBS volumes are bound to a specific AZ.

![](/img/04/64.png)

Initially, the volume will not be attached, but after refreshing, it will be available. Since it is now available but not yet attached, I can go to Actions and then select Attach Volume. I need to find the instance to which I want to attach it. 

![](/img/04/65.png)

We have one running right here, so I'll attach this volume to my instance by clicking Attach Volume. 

![](/img/04/66.png)

Voilà! Our instance now has two EBS volumes attached to it.

![](/img/04/67.png)

To confirm this, I can refresh the page, go to Storage on my EC2 console, and scroll down. Now, under block devices, I see two block devices: one of 8 GB and one of 2 GB.

To actually use this new block device, it requires additional steps that are a bit more complicated and out of scope for this course. However, you can search for instructions on "[Format EBS Volume Attach EC2](https://docs.aws.amazon.com/ebs/latest/userguide/ebs-using-volumes.html)" which will guide you on how to make an Amazon EBS volume available for use on Linux.

![](/img/04/68.png)

Now, let's try something different. If I create another volume, again 2 GB of GP2, but this time with the Availability Zone set to EU West 1A instead of EU West 1B, it will be in a different AZ than my EC2 instance. The reason I'm doing this is to show that EBS volumes are indeed bound by a specific Availability Zone.

Let me refresh this. The new volume is available in a different AZ, EU West 1A. If I try to attach it to my EC2 instance, you'll notice that I cannot do so because my EC2 instance is in EU West 1B. This confirms that EBS volumes are bound to specific Availability Zones.

Lastly, I can take this volume, select Action, choose Delete Volume, and it will be gone. This demonstrates the power of the cloud—you can request and delete volumes on the go in a matter of seconds. 

Now, with our two EBS volumes here, I want to show you a cool behavior. What happens if I terminate my instance? Remember, the root volume of 8 GB has the Delete on Termination attribute enabled.

--

To verify this, go to Storage, then Block Devices, and scroll all the way to the right. You'll see that the first volume has Delete on Termination set to "Yes," while the second volume does not. Why is this one set to "Yes"? 

![](/img/04/69.png)

Well, during the instance **`launch process`**, when you scroll down to the Storage section and click on Advanced, you’ll see that the root volume of 8 GB has this attribute set to "Yes" by default. This makes sense, but you could change it to "No" if you wanted to keep the root volume after terminating your instance.

This explains why the first volume has "Yes" in the table. So, if I go ahead and terminate my instance (which I will), it will successfully terminate, removing it from here. I can then go back to my EBS volumes and refresh. Soon, the 8 GB volume will be detached and then terminated.

![](/img/04/70.png)

So, if I go ahead and terminate my instance (which I will), it will successfully terminate, removing it from here.

![](/img/04/71.png)

I can then go back to my EBS volumes and refresh. Soon, the 8 GB volume will be detached and then terminated.

After a short pause, you'll see that the 8 GB volume has disappeared, leaving only the 2 GB volume. If I return to my EC2 console, it will show that my first instance has been terminated.

![](/img/04/73.png)


#### EBS Snapshots Overview

* Make a backup (snapshot) of your EBS volume at a point in time
* Not necessary to detach volume to do snapshot, but recommended 
* Can copy snapshots across AZ or Region

![](/img/04/74.png)


**EBS Snapshots Features**

![](/img/04/75.png)

#### EBS Snapshots Hands On

![](/img/04/76.png)

So we have this 2GB GP2 EBS volume available to us, and we can take a snapshot of it. To do this, go to `Actions` and select `Create Snapshot`. You can add a description, for example, "Demo Snapshot," and then click Create Snapshot. 

Next, in the left-hand side menu, instead of Volumes, you can click on Snapshots. The Snapshots section shows you a list of all the snapshots you have. As you can see, we have one here. It is completed, 100% available, and provides some information about the snapshot itself.

![](/img/04/78.png)

First of all, what we can do is copy this snapshot to other regions. If you right-click and select Copy Snapshot, you can copy this snapshot to any destination region that you want. This can be very handy if, for example, you want to implement a disaster recovery strategy to ensure your data is backed up in another region of AWS. 

Although I won’t do this now, you get the idea. 

![](/img/04/79.png)


Another thing we can do is take this snapshot and recreate a volume from it. Go to Actions and select Create Volume from Snapshot. 

![](/img/04/80.png)

Choose a 2GB GP2 volume. The target AZ doesn’t have to remain EU West 1A; it can be, for example, EU West 1B. You can also include this volume and add some tags if you want. Once you click Create Volume, what will happen is that if we go back to our Volumes section, we now have two volumes. 

![](/img/04/81.png)

One of them, this one, was restored from a snapshot, and it is in EU West 1B. The idea is that, thanks to snapshots, we can "copy" EBS volumes across different availability zones, which is very handy.

![](/img/04/82.png)

If we look again at Snapshots, we can have a look at what's called the Recycle Bin. The Recycle Bin is a way for you to protect your EBS snapshots from accidental deletion, as well as your Amazon Machine Images.

![](/img/04/83.png)

You can create a retention rule

![](/img/04/84.png)

You can create a retention rule and name it "Demo Retention Rule." I will select EBS snapshots, apply it to all resources, and retain them for one day. For the rule settings, I will leave it unlocked so I can delete the rule whenever I want. Then, click `Create Retention Rule`. 

![](/img/04/85.png)

Now, under `Resources`, we can see if we have resources in the `Recycle Bin`.

![](/img/04/86.png)

Let’s go back to our Snapshots in the `EC2` console. I'll navigate to EC2, then to Snapshots. One more shortcut: before I delete the snapshot, I want to show you the storage tier. Right now, it is in the standard storage tier. However, you can move the storage tier by archiving the snapshot, which will allow you to move it to a different pricing level. If you want to restore it, though, you will need to wait 24 to 72 hours.

![](/img/04/87.png)

![](/img/04/88.png)

So, let’s go ahead **Actions** and **delete the snapshot**. As you can see, it's gone. 

![](/img/04/89.png)

Previously, when you deleted a snapshot, it was permanently removed and couldn't be recovered. Now, thanks to the Recycle Bin, if I refresh my resources, I can see that my snapshot has reappeared. I can click on it and choose Recover Resources.

![](/img/04/90.png)

Voila! It's back in my snapshots on my EC2 console. 

![](/img/04/91.png)

Okay, that was pretty awesome, right? That’s it for EBS snapshots. I hope you liked it, and I’ll see you in the next lecture.

#### AMI Overview

* AMI = Amazon Machine Image
* AMI are a customization of an EC2 instance
  * You add your own software, configuration, operating system, monitoring... 
  * Faster boot / configuration time because all your software is pre-packaged
* AMI are built for a specific region (and can be copied across regions)
* You can launch EC2 instances from:
  * A Public AMI: AWS provided
  * Your own AMI: you make and maintain them yourself
  * An AWS Marketplace AMI: an AMI someone else made (and potentially sells)

**AMI Process (from an EC2 instance)**

* Start an EC2 instance and customize it
* Stop the instance (for data integrity)
* Build an AMI – this will also create EBS snapshots • Launch instances from other AMIs

![](/img/04/92.png)

#### AMI Hands On

So let's go ahead and practice using AMI. I'm going to `launch an instance` and go through this new experience. 
* I'll scroll down and choose Amazon Linux 2. 
* Then, I'll scroll down again. What is the key to micro? I'll select the EC2 tool as my key pair, but it doesn't really matter. 
* Next, I’ll scroll down, edit the `network settings`, 
  * and select an existing security group—my `Launch Wizard 1` from before. 

The storage settings remain the same. For advanced details, I will scroll down and go to user data. This time, you're going to copy everything except the last line. 

```sh
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
```

In the first four lines, we actually install HTTPD, which is the Apache web server. The last line creates an index file, but right now, we don't want to create an index file. We want to do everything but that so we can create an AMI out of it. So just copy everything except the last line, which is the systemctl command. Then, we launch our instance.

![](/img/04/93.png)

So our instance is launched, and what's going to happen is that the instance will start, and then it will run through the EC2 user script to install the Apache web server. If I'm too quick and try to open this public IPv4 right now, and try to enter it, as you can see, it doesn't work. 

![](/img/04/94.png)

I'll get a connection error, a refusal, and so on. I need to make sure I'm also using the HTTP protocol, of course. But it just won't work, right, because you need to give it a bit of time. Even if it says running, you need to wait for the EC2 user data script to run for the first time. This might take a minute or two, but don't rush—just wait for it to be done. Then, at some point, when you refresh, you will see the screen. It took about two minutes, but now I have my test page. This is the basic page from the Apache web server, so we're good to go.

![](/img/04/97.png)

Now, what we're going to do is create an AMI because we want to save the state of our EC2 instance and reuse it. So I right-click, go to Image and Template, and then select Create Image. 

![](/img/04/95.png)

We'll call this one "demo image," and we're going to create our own AMI. The settings right here can be left as is. Click Create Image. 

![](/img/04/96.png)

Now, an AMI is being created. If I go to the left-hand side and click on AMIs, we can see that my demo AMI is registered. Right now, the status is pending because it is being created. We need to be patient and wait for it to reach the created state.

Once my Amazon AMI is created, I can launch instances from this AMI by clicking here. 

![](/img/04/98.png)

Alternatively, if you are on the instance creation page, you can launch instances from AMI. 

In the Quick Start tab, we have access to the ones we know, but we can also go to the My AMIs tab. Under "Owned by me," you can choose the demo image you just created. Scroll down, select a key pair or not—it's up to you. Network settings can be edited again, and we'll select the existing Launch Wizard 1 security group.

![](/img/04/99.png)

![](/img/04/100.png)

In the advanced settings at the very bottom, I'll enter some user data. I copy the first three lines, which start with a hash, and then the last line, which is the echo on a new line. What we’re doing is simply writing a new file; we don’t need to reinstall HTTPD because this AMI already contains HTTPD, which speeds up the boot time. This is why you would create an AMI. We launch the instance, and now the instance is launched, so I can click on it. 

![](/img/04/101.png)

```sh
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

This is the one from the AMI. I need to wait for it to be fully created. Once my instance from the AMI is running, I take the public IP address, and then I see the "Hello World" message. As you can see, this was much quicker because we didn’t have to install HTTPD again.

![](/img/04/102.png)

![](/img/04/103.png)

This demonstrates the power of AMIs. You can imagine using this process for more than just HTTPD—it could be security software, a lot of pre-installed software, and so on. You install it, maybe it takes two or three minutes, then package it as an AMI. When you start from the AMI, you might do some end customization, but you get a much faster boot time, and you're good to go.

So let's wrap up this demo. To clean up, take your two instances and terminate them. That’s it. I’ll see you in the next lecture.

---

#### EC2 Image Builder

* Used to automate the creation ofVirtual Machines or container images
* => Automate the creation, maintain, validate and test EC2 AMIs
* Can be run on a schedule (weekly, whenever packages are updated, etc...) 
* Free service (only pay for the underlying resources)


![](/img/04/104.png)

--

Okay, let’s talk about a new service that I really like and that is now included in the exam: EC2 Image Builder. This service is used to automate the creation of virtual machines or container images. So, what does that mean for the exam? It means that with EC2 Image Builder, you can automate the creation, maintenance, validation, and testing of AMIs for EC2 instances.

Let’s take a closer look at how this works through a diagram. EC2 Image Builder is the service that manages the entire process. When it runs, it automatically creates an EC2 instance called a Builder EC2 Instance. This instance is responsible for building components and customizing the software. For example, it might install Java, update the CLI, apply system updates, install firewalls, or even deploy your application—whatever you’ve defined in the process. Once this customization is done, an AMI is created from that EC2 instance. But remember, all of this is automated.

After the AMI is created, it needs to be validated. EC2 Image Builder will automatically launch a Test EC2 Instance from that AMI and run a series of tests that you have pre-defined. If you don’t want to run any tests, you can skip this step. However, these tests can be crucial—they might check if the AMI is working properly, if it’s secure, if your application is running correctly, and so on. Once the AMI passes all the tests, it is then ready to be distributed.

Although EC2 Image Builder is a regional service, you can distribute the AMI to multiple regions. This capability allows your application and workflow to be truly scalable and available across different geographical areas.

Additionally, EC2 Image Builder can be run on a schedule. You can define a weekly schedule, set it to run whenever packages are updated, or trigger it manually. It’s a flexible service that adapts to your needs.

One important point to note is that EC2 Image Builder itself is a free service. However, you will incur costs for the underlying resources it uses. What does this mean? It means that when an EC2 instance is created during this process (and EC2 Image Builder will create these instances), you will be charged for the EC2 instances. Similarly, once the AMI is created and distributed, you’ll pay for the storage of that AMI in every region where it is stored. But this should all make sense, right?


#### EC2 Instance Store

* EBS volumes are network drives with good but “limited” performance
* If you need a high-performance hardware disk, use EC2 Instance Store
* Better I/O performance
* EC2 Instance Store lose their storage if they’re stopped (ephemeral)
* Good for buffer / cache / scratch data / temporary content
* Risk of data loss if hardware fails
* Backups and Replication are your responsibility

We've discussed how to attach a network drive to our EC2 instances, which offers good performance—though sometimes, you might need even higher performance. For those cases, you can use a hardware disk directly attached to your EC2 instance.

Although an EC2 instance is a virtual machine, it is connected to a physical server, and some of these servers have disk space that is physically attached to them. A special type of EC2 instance can leverage something called an EC2 Instance Store, which refers to this hardware disk attached directly to the physical server.

Using an EC2 instance store provides significantly better I/O performance and higher throughput, making it an excellent choice when you need extremely high disk performance. However, there’s a caveat: if you stop or terminate an EC2 instance that uses an instance store, the storage will be lost—hence the term "ephemeral storage." This means that an EC2 instance store is not suitable for durable, long-term data storage.

So, when is it appropriate to use an EC2 instance store? It’s ideal for scenarios where you need a buffer, a cache, scratch data, or temporary content. But for long-term storage, services like EBS (Elastic Block Store) are more appropriate.

It’s also important to note that if the underlying server of your EC2 instance fails, you risk losing the data stored on the instance store because the storage is tied directly to that specific server. Therefore, if you choose to use an EC2 instance store, it’s your responsibility to back up the data and replicate it as needed.

To give you an idea of the performance difference, consider the i3 instance type, which comes with an instance store. The read and write IOPS (input/output operations per second) for these instances can reach up to 3.3 million and 1.4 million IOPS, respectively, for the most performant options. In comparison, an EBS volume of type GP2 can reach up to 32,000 IOPS, which is significantly lower. This example is just to illustrate the substantial performance difference.

**Local EC2 Instance Store**

![](/img/04/105.png)

From an exam perspective, whenever you encounter a scenario requiring very high-performance hardware-attached volumes for your EC2 instances, think of the local EC2 Instance Store.


#### EFS – Overview


**EFS – Elastic File System**

* Managed NFS (network file system) that can be mounted on 100s of EC2
* EFS works with Linux EC2 instances in multi-AZ
* Highly available, scalable, expensive (3x gp2), pay per use, no capacity planning

--

Now, let’s talk about a third type of storage you can attach to an EC2 instance: a network file system called EFS (Elastic File System). EFS is a managed network file system, and its key advantage is that it can be mounted to hundreds of EC2 instances simultaneously.

Unlike an EBS volume, which can only be attached to a single EC2 instance at a time, an EFS drive can be shared across multiple EC2 instances, making it a shared network file system or shared EFS. This feature is particularly useful for scenarios where multiple instances need to access the same data.

EFS is designed to work with your Linux EC2 instances and can function across multiple availability zones (AZs). This means that an instance in one AZ can access the same EFS volume as an instance in another AZ, providing high availability and redundancy.

While EFS is highly available, scalable, and easy to use, it is also relatively expensive—about three times the cost of a GP2 EBS volume. However, with EFS, you pay based on your usage rather than for a predefined capacity. For instance, if you store 20 gigabytes of data on your EFS drive, you only pay for those 20 gigabytes.

--

To visualize this, imagine an EFS file system with its own security group. You could have EC2 instances in different availability zones, say, us-east-1a, us-east-1b, and us-east-1c, all connected to the same EFS file system. This setup allows all these instances to share the same data seamlessly.


![](/img/04/106.png)

**EBS vs EFS**

Now let's outline the exact differences between EBS (Elastic Block Store) and EFS (Elastic File System).

With EBS, if you have two EC2 instances in one Availability Zone (AZ) and another instance in a different AZ, the EBS volume can only be attached to one instance within a specific AZ at a time. EBS volumes are bound to the AZ they were created in. If you want to move an EBS volume from one AZ to another, you would create a snapshot of the EBS volume, then restore that snapshot into the new AZ. This process effectively moves the EBS volume to a different AZ, but it’s important to note that this is a copy, not an in-sync replica. This means that the EBS volume in the new AZ is independent, and the original volume cannot be used by another EC2 instance in a different AZ simultaneously.

On the other hand, EFS is a network file system, which means that whatever is stored on the EFS drive is shared across all instances that have it mounted. For example, if you have many instances in Availability Zone 1 and others in Availability Zone 2, all of these instances can mount the same EFS drive using a mount target, and they will all see the same files. This makes EFS a shared file system, allowing multiple instances across different AZs to access the same data simultaneously.

Hopefully, this explanation makes the differences between EBS and EFS clear. Understanding this is important, as the exam may test you on these concepts.

![](/img/04/107.png)


**EFS Infrequent Access (EFS-IA)**

![](/img/04/108.png)


Additionally, there’s a storage class you need to know about for EFS: EFS Infrequent Access (EFS-IA). This storage class is cost-optimized for files that you don’t access very often—perhaps not every day. EFS-IA offers up to 92% lower costs for storing data compared to the EFS Standard storage class.

If you enable EFS-IA, EFS will automatically move your files to EFS-IA based on the last time they were accessed, according to a lifecycle policy that you define. For instance, imagine you have an EFS file system with three files in EFS Standard and a fourth file that hasn’t been accessed for 60 days. If your lifecycle policy is configured to move files to EFS-IA after 60 days of inactivity, this fourth file will be moved to EFS-IA, resulting in cost savings.

The process is automatic, and the next time you access this file, it will be moved back into EFS Standard, assuming it is accessed frequently. The key point here is that this is a cost-saving optimization, and from an application perspective, it’s completely transparent. Your applications don’t need to know whether the file is in EFS Standard or EFS-IA—they access files in the same way regardless of the storage class. The cost optimizations are handled behind the scenes by EFS.

This is an important concept to understand for the exam. I hope you found this explanation helpful, and I will see you in the next lecture.


#### Shared Responsibility Model for EC2 Storage

![](/img/04/110.png)

Understanding the shared responsibility model is crucial for the Certified Cloud Practitioner exam, especially when it comes to EC2 storage. This model helps clarify which security and management tasks are handled by AWS and which are the customer’s responsibility.

**AWS’s Responsibilities:**

Infrastructure Management: AWS is responsible for maintaining the underlying infrastructure that powers EC2 instances, EBS, and EFS. This includes the physical servers, networking, and storage hardware.

Data Replication: AWS is responsible for replicating data across multiple hardware components, as specified in the technical documentation for services like EBS and EFS. This ensures that if one piece of hardware fails, your data remains accessible and you, as a customer, are not impacted.

Hardware Maintenance: If an EBS volume or part of it fails due to hardware issues, AWS is responsible for replacing the faulty hardware to ensure continued service availability.

Data Access Security: AWS must ensure that their employees do not have unauthorized access to your data. This includes enforcing strict access controls and maintaining robust security protocols.

**Customer Responsibilities:**

Backup and Snapshots: It is your responsibility to set up and manage backup and snapshot procedures to protect your data. Regular backups are essential to prevent data loss.

Data Encryption: Implementing data encryption is also your responsibility. Encrypting your data adds an additional layer of security, ensuring that even if data were somehow accessed by unauthorized parties, it remains protected. AWS provides tools for encryption, but enabling and managing encryption is up to you.

Data Management: Any data you store on an EBS or EFS drive, and anything you write to those disks, is your responsibility. This includes managing the data lifecycle and ensuring that your data is secure.

EC2 Instance Store Considerations: If you use an EC2 instance store, you must be aware of the associated risks. Data stored on an instance store is ephemeral, meaning it can be lost if the underlying hardware fails, or if you stop or terminate the EC2 instance. Therefore, it is your responsibility to back up any critical data stored in an instance store.

Understanding these responsibilities is critical not only for the exam but also for effectively managing your resources on AWS. Knowing where your duties lie helps ensure that your data remains secure and your applications run smoothly.


#### Amazon FSx Overview

* Launch 3rd party high-performance file systems on AWS 
* Fully managed service

![](/img/04/111.png)

**Amazon FSx for Windows File Server**

![](/img/04/113.png)

**Amazon FSx for Lustre**

![](/img/04/112.png)


#### EC2 Instance Storage - Summary

* EBS volumes:
  * network drives attached to one EC2 instance at a time
  * MappedtoanAvailabilityZones
  * Can use EBS Snapshots for backups / transferring EBS volumes across AZ
* AMI: create ready-to-use EC2 instances with our customizations
* EC2 Image Builder : automatically build, test and distribute AMIs
* EC2 Instance Store:
  * High performance hardware disk attached to our EC2 instance 
  * Lost if our instance is stopped / terminated
* EFS: network file system, can be attached to 100s of instances in a region 
* EFS-IA: cost-optimized storage class for infrequent accessed files
* FSx for Windows: Network File System for Windows servers
* FSx for Lustre: High Performance Computing Linux file system

#### Section Cleanup

Let's do a quick cleanup to ensure we have a clean slate and avoid any unnecessary costs in the future.

1. **EC2 Dashboard**: Start by going to the EC2 dashboard where you can see all the resources running in your region. Here’s what you need to check:

   * **Running Instances**: If you see any running instances (e.g., two instances), open this in a new tab.
   * **Volumes**: If you have any EBS volumes (e.g., four volumes), open this in a new tab as well.
   * **Key Pairs**: Key pairs do not incur any costs, so you can leave them as is.
   * **Snapshots**: If you have any snapshots (e.g., two snapshots), open this in a new tab.
   * **Security Groups**: Security groups generally don’t cost money, so you can leave them as is.

![](/img/04/114.png)

**Terminate EC2 Instances:**

In the EC2 Instances tab, select the instances you want to terminate. Right-click on them and choose Terminate.


**Delete EBS Volumes:**

After terminating the instances, some root EBS volumes will automatically be deleted. However, for any additional EBS volumes that are not attached to an instance, you will need to delete them manually.

![](/img/04/115.png)

**Delete Snapshots:**

Go to the Snapshots tab and select the snapshots you want to delete. Choose Actions and then Delete Snapshot. If you encounter an error stating that a snapshot cannot be deleted because it’s being used by an AMI, proceed to the next step.

![](/img/04/116.png)

![](/img/04/117.png)

**Deregister AMIs:**

Go to the AMIs section on the left-hand side. Find the AMI that’s using the snapshot, and deregister it. Confirm the deregistration.
Return to the Snapshots tab and delete the snapshot that was previously locked.


![](/img/04/118.png)

Now -> **Delete Snapshots:**

Final Check:

* Go back to the EC2 Instances tab to ensure all instances are terminated.
* Check the Volumes tab to confirm all EBS volumes are deleted.
* Verify that no Snapshots or AMIs remain.

Refresh your EC2 dashboard, and if everything is clear—no running instances, volumes, snapshots, or AMIs—you’re good to go.

That’s it for the cleanup. Everything should be in order now. See you in the next lecture!


### Elastic Load Balancing & Auto Scaling Groups Section

This is the section where we really see the power of the AWS cloud and the cloud in general and see how these new paradigms we discussed really help us shine and make our applications scale seamlessly. So let's discuss the concepts of scalability and high availability.

**Scalability & High Availability**

* Scalability means that an application / system can handle greater loads by adapting.
* There are two kinds of scalability: • Vertical Scalability
  * Horizontal Scalability (= elasticity)
  * Scalability is linked but different to High Availability
* Let’s deep dive into the distinction, using a call center as an example

If your application can scale, it means that it can handle greater loads by adapting. There are two kinds of scalability in the cloud: vertical scalability and horizontal scalability, also called elasticity. Scalability is linked, but different, from high availability, and these concepts will be discussed in this section. Let's do a deep dive, and we'll use a call center as an example.

Imagine we have a call center, and we just received a call. Now let's see what it means to be scalable in that case.

**Vertical Scalability**

* Vertical Scalability means increasing the size of the instance
* For example, your application runs on a t2.micro
* Scaling that application vertically means running it on a t2.large
* Vertical scalability is very common for non distributed systems, such as a database.
* There’s usually a limit to how much you can vertically scale (hardware limit)
  
![](/img/05/01.png)

First, let's deal with vertical scalability. In AWS, when you are vertically scalable, it means that you can increase the size of the instance. So for our call center, say we have a junior operator, and if we were able to upgrade that operator, we would get a senior operator. For example, the senior operator can handle a lot more calls than the junior operator because they are more experienced. This is what vertical scalability looks like in a call center—if we could upgrade, obviously, a junior operator into a senior operator. In AWS, for example, say your application runs on a T2 micro, and to achieve vertical scalability for that application, you would run your application on a T2 large. So we've changed the size of our EC2 instance. Vertical scalability is very common when you have a non-distributed system, such as a database. If you want to improve the performance of your database, you would increase its size. However, with vertical scalability, there is usually a limit to how much you can scale vertically, and that limit is determined by the hardware, even though these limits can be very, very high nowadays.


**Horizontal Scalability**

• Horizontal Scalability means increasing the number of instances / systems for your application
• Horizontal scaling implies distributed systems.
• This is very common for web applications / modern applications
• It’s easy to horizontally scale thanks the cloud offerings such as Amazon EC2

![](/img/05/02.png)

Next is horizontal scalability. Instead of increasing the size of your EC2 instance, you increase the number of instances or systems for your application. Going back to our call center example, if we have one operator and want to scale horizontally, we would add another operator. If we need to handle more calls, we would add yet another operator, and so on. Maybe we can scale horizontally from one operator to six operators. Horizontal scaling implies, as you can see on the right-hand side, that you need to have a distributed system. For a call center, this makes sense—each operator can take calls independently. In AWS, horizontal scaling is very common for web applications or modern applications, which are usually designed with horizontal scalability in mind. Scaling on AWS is made easy thanks to Amazon EC2 and auto-scaling groups, which we'll explore in this section.

**High Availability**


* High Availability usually goes hand in hand with horizontal scaling
* High availability means running your application / system in at least 2 Availability Zones
* The goal of high availability is to survive a data center loss (disaster)

![](/img/05/03.png)

Now let's talk about high availability, which goes hand-in-hand with horizontal scaling. High availability means that you are running your application system in at least two availability zones on AWS. For our call center, this would mean having a call center in New York and maybe a second one in San Francisco. If one of these call centers goes down—for example, due to a power outage in New York—we can still take calls in San Francisco, thus ensuring high availability. While San Francisco may be busier, we are at least surviving the disaster of a power outage in one of our buildings. In AWS, we use two availability zones to achieve this, with the goal of surviving a data center loss or disaster. In AWS, this disaster could be an earthquake, a power outage, or various other issues.

**High Availability & Scalability For EC2**

* Vertical Scaling: Increase instance size (= scale up / down) 
  * From: t2.nano - 0.5G of RAM, 1 vCPU
  * To: u-12tb1.metal – 12.3 TB of RAM, 448 vCPUs
* Horizontal Scaling: Increase number of instances (= scale out / in) 
  * Auto Scaling Group
  * Load Balancer
* High Availability: Run instances for the same application across multi AZ
  * Auto Scaling Group multi AZ
  * Load Balancer multi AZ

To summarize, high availability** and scalability for EC2 involve:

* **Vertical Scaling**: Increasing the instance size. You can scale up (increasing) or scale down (decreasing). For example, you can go from a T2 nano with 0.5 GB of RAM and one vCPU to a U-12tb1.metal, which has 12.3 terabytes of RAM and 448 vCPUs. This is vertical scalability.
* **Horizontal Scaling**: Increasing the number of instances, known as scaling out, or decreasing the number of instances, known as scaling in. This involves using an auto-scaling group and a load balancer. This is the topic of this section.
* **High Availability**: Running instances of the same application across multiple availability zones. This is achieved by leveraging an auto-scaling group in multi-AZ mode and a load balancer in multi-AZ mode.

**Scalability vs Elasticity (vs Agility)**

One last word. It's important to distinguish between scalability, elasticity, and agility. To summarize:

* **Scalability**: The ability of a system to accommodate a larger load by making the hardware stronger (scaling up) or by adding nodes (scaling out). This means your application can scale.
* **Elasticity**: A cloud-native concept where, once a system is scalable (either scaling up or out), it automatically scales based on the load it receives. This allows you to pay per use, match the demand with the right number of servers, and optimize costs. Elasticity is a key concept in AWS.
* **Agility**: Although not directly related to scalability or elasticity, agility refers to the ability to quickly provision new IT resources, reducing the time to make resources available from weeks to minutes. This makes your organization more agile, enabling quicker iterations and faster progress.

That's it for this section of the introduction. I hope you liked it, and I will see you in the next section.


#### Elastic Load Balancing (ELB) Overview

**What is load balancing?**

![](/img/05/04.png)

So let's see the first service that will allow us to be more elastic on AWS. This is called Elastic Load Balancing. A load balancer is a server that will forward internet traffic down to multiple servers downstream, which, in this context, will be EC2 instances. These instances are also called the back-end EC2 instances. Elastic Load Balancing is managed by AWS. We have a load balancer, which is what we will be publicly exposing to our users. Behind that load balancer, we will have multiple EC2 instances—maybe three in this case.

When our first user interacts with the load balancer, the load balancer will direct the traffic to one of these EC2 instances. The EC2 instance will respond, and the user will receive the response. Now, if a second user comes in, the response will come from another EC2 instance, and if a third user comes in, as you can expect, the response will come from yet another EC2 instance. The load balancer distributes the incoming traffic across multiple EC2 instances, which allows us to better scale our back-end.

**Why use a load balancer?**

* Spread load across multiple downstream instances
* Expose a single point of access (DNS) to your application • Seamlessly handle failures of downstream instances
* Do regular health checks to your instances
* Provide SSL termination (HTTPS) for your websites
* High availability across zones

You can spread the load across multiple downstream instances.
You can expose a single point of access (a DNS hostname) for your application.
You can seamlessly handle the failures of downstream instances by performing regular health checks on them. If an instance fails, the load balancer will not direct traffic to it, thus hiding the failure of an EC2 instance.
You can easily provide SSL termination (HTTPS) for your websites.
You can use a load balancer across multiple availability zones, making your application highly available.


**Why use an Elastic Load Balancer?**

* An ELB (Elastic Load Balancer) is a `managed load balancer`
  * AWS guarantees that it will be working
  * AWS takes care of upgrades, maintenance, high availability 
  * AWS provides only a few configuration knobs
* It costs less to setup your own load balancer but it will be a lot more effort on your end (maintenance, integrations)
* 4 kinds of load balancers offered by AWS:
  * Application Load Balancer (HTTP / HTTPS only) – Layer 7
  * Network Load Balancer (ultra-high performance, allows for TCP) – Layer 4
  * Gateway Load Balancer – Layer 3
  * Classic Load Balancer (retired in 2023) – Layer 4 & 7

![](/img/05/05.png)

Elastic Load Balancing is a managed service, so you don't need to provision servers—AWS takes care of that. AWS guarantees that the load balancer will work, handling all upgrades, maintenance, and high availability. The only thing we need to do is configure a few settings for the load balancer's behavior. While it’s possible to set up your own load balancer on EC2, using ELB is generally less expensive and saves you a lot of effort in terms of maintenance, integration, and operating system upgrades.

AWS offers four types of load balancers, and it’s important to know the differences between them:

1. Application Load Balancer (ALB): For HTTP and HTTPS-only traffic, this is a layer 7 load balancer because it operates at the application layer (HTTP/HTTPS).
2. Network Load Balancer (NLB): Known for ultra-high performance, it operates at layer 4 and handles TCP and UDP traffic.
3. Gateway Load Balancer (GWLB): Operates at layer 3 and is used to route traffic to security virtual appliances like firewalls.
4. Classic Load Balancer (CLB): A legacy load balancer that supported both layer 4 and layer 7 traffic. However, it’s being retired in 2023 and is no longer relevant for the exam, as it has been replaced by ALB and NLB.


---

**Exam Key Points:**

* **ALB (Application Load Balancer)**: If you see references to HTTPS, HTTP, or gRPC protocols, it’s layer 7, so it’s the ALB. It's also the choice when you need HTTP routing features or a static DNS hostname.
* **NLB (Network Load Balancer)**: Operates at layer 4 (TCP/UDP) and is ideal for scenarios requiring ultra-high performance, capable of handling millions of requests per second. It provides a static IP address through the use of Elastic IPs.
* **GWLB (Gateway Load Balancer)**: Operates at layer 3 using the GENEVE protocol for IP packet handling. It's used to route traffic to firewalls or other third-party security virtual appliances for tasks such as intrusion detection or deep packet inspection.

**How They Work:**

* **ALB and NLB**: Users access the load balancers on the specified protocols (HTTP/HTTPS for ALB, TCP/UDP for NLB). The load balancers route traffic to the downstream EC2 instances.

* **GWLB**: The Gateway Load Balancer directs traffic to virtual appliances running on EC2 instances (e.g., firewalls). After processing the traffic, it forwards it back to the GWLB, which then routes it to the final application.

Understanding these differences between load balancers is crucial for the exam. If you've grasped these concepts, you’re well-prepared for related exam questions. I will see you in the next lecture for some questions.

#### Application Load Balancer (ALB) Hands On

So we're going to practice launching a load balancer, but first, we need to send traffic to something. So first, we're going to launch EC2 instances. I'll go into "Launch Instances" and launch two instances. On the right-hand side, I can see two instances, and the name for the first one will be "my first instance." We'll rename the second one later. We're going to use Amazon Linux 2. On this architecture, we'll use a T2 micro, and we'll proceed without a T2 key pair since we don't need SSH capability. We can use EC2 instances whenever we need to. For network settings, we'll select an existing security group and use the Launch Wizard 1 security group, which allows HTTP and SSH traffic into our EC2 instance. So that's perfect. We're going to use the basic storage settings. For advanced details, I'll scroll down and add some EC2 user data. I'll copy what I have here and paste it. 

```sh
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

![](/img/05/07.png)
![](/img/05/08.png)
![](/img/05/09.png)


This will launch the EC2 instance the same way we did before using this EC2 user data script. Now let's launch our two instances. Next, we're going to view all instances. I'll rename the second one "my second instance" and save it. Let's wait for these instances to be ready.


![](/img/05/10.png)

Now, my EC2 instances are ready. I'll copy the first IPv4 address, paste it into a browser, and visit the URL. As you can see, I get a "hello world" message from my instance, which is great. 

![](/img/05/11.png)

Then, I'll go to my second instance, copy the IPv4 address, paste it, press enter, and I get "hello world" again. As you can see, both instances give us "hello world" messages.

![](/img/05/12.png)

The last part is checking, and what we'd like to do is have only one URL to access these two EC2 instances and balance the load between them. For this, of course, we'll use a load balancer. Let's scroll down and look at load balancers. Here, you can create a load balancer. 

![](/img/05/13.png)

We have different load balancer types. In this demo, we're going to focus only on the application load balancer.

You need to understand the difference between the `ALB`, the `network load balancer`, and `the gateway load balancer`. 

* **The application load balancer** is for HTTP and HTTPS traffic. 
* **The network load balancer** is for the TCP and UDP protocol, or TLS over TCP. This is something you're going to use when you need ultra-high performance, meaning millions of requests per second while maintaining ultra-low latency.
* **The gateway load balancer** is used for security, intrusion detection, firewalls, and so on. It analyzes network traffic. The classic load balancer, by the time you watch this video, may be gone because it's being phased out. Therefore, I'm not going to discuss it.

![](/img/05/15.png)


Let's focus on creating the application **load balancer**. 

I'm going to call this one "Demo ALB." If you want to read about how load balancing works, you can do so, but hopefully, the previous lecture was enough for you. The scheme is internet-facing, and the address type is IPv4.

![](/img/05/16.png)

For network mapping, we need to decide where to deploy the load balancer and how many availability zones to use. Let's deploy it in all of them. Great.

![](/img/05/17.png)

![](/img/05/18.png)

 I'm going to create a new security group for it, and we only need to allow HTTP traffic. I'm going to call it "DemoSGLoadBalancer," allowing HTTP into the ALB. The inbound rule will allow all HTTP from anywhere. The outbound rule is fine. Let's create this security group.

![](/img/05/19.png)

Now that it's created, I can go back here, refresh the page, choose my "DemoSGLoadBalancer," and remove the default security group so that I'm left with only one security group.

![](/img/05/20.png)

Let's scroll down, and we are under listeners and routing. We need to route the traffic from HTTP on port 80 to a target group. A target group is nothing more than a group of my EC2 instances that were created. For this, we need to create a target group. Let's click here to create one.

![](/img/05/21.png)

The basic configuration tells us that we want to group instances together. You have other options, but we want to group instances together, and I'll call this one "DemoTGALB." The protocol is HTTP on port 80. There are different options, but based on the option you choose, it's going to be a target group for a different kind of load balancer. We'll keep it as HTTP on port 80, with the HTTP version as 1. The health check is good. Let's click on "Next."



![](/img/05/22.png)


![](/img/05/23.png)

We need to register our targets, so we're going to register both EC2 instances on port 80 and include them as pending below. Now, my instances are registered, and let's create this target group. 

![](/img/05/24.png)

Let's create it. 

![](/img/05/25.png)

Now, I need to refresh my page. The one I want to use is "DemoTGALB." This target is created, and it's linked to the listener on my load balancer on port 80. 

![](/img/05/26.png)


Now I'm good to go, and I can go ahead and `create my load balancer`.

I'll click on "View Load Balancer," and I'm back on this page where I can look at my load balancer. Right now, it is in the provisioning phase, so we need to wait until it is provisioned.

![](/img/05/28.png)


My ALB is now active. It's ready. As you can see, there's a DNS name available for me. I'm going to copy this, paste it into a new tab, and through the application load balancer, I'm able to get a LOL. The cool thing about it is that if I refresh this page and keep on refreshing it, the target is changing. That's because my application load balancer is redirecting between both my EC2 instances, which is very cool, and that's proof that load balancing is happening.

How do we know? If we go to our target group and look at the targets of my target group, both are healthy. This means that the application load balancer, through the target group, is sending traffic to both of them, one after the other. The target group is very smart because if I take my first instance and stop it, it's going to be unhealthy because it can't respond to the incoming traffic.



#### uuu

**What’s an Auto Scaling Group?**
* In real-life, the load on your websites and application can change
* In the cloud, you can create and get rid of servers very quickly
* The goal of an Auto Scaling Group (ASG) is to:
  * Scale out (add EC2 instances) to match an increased load
  * Scale in (remove EC2 instances) to match a decreased load
  * Ensure we have a minimum and a maximum number of machines running 
  * Automatically register new instances to a load balancer
  * Replace unhealthy instances
* Cost Savings: only run at an optimal capacity (principle of the cloud)


**Auto Scaling Group in AWS**

![](/img/05/06.png)


**Auto Scaling Group in AWS With Load Balancer**