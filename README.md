## AWS Certified Cloud Practitioner CLF-C02

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


### IAM Section

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

### IAM Policies inheritance

Okay, let's now discuss IAM policies in depth. Imagine we have a group of developers—Alice, Bob, and Charles—and we attach a policy at the group level. In this case, the policy will be applied to every member of the group. So Alice, Bob, and Charles will all get access and inherit this policy. If you have a second group, such as operations, with a different policy, David and Edward will have a different policy from the developers' group. If Fred is a user, he has the option not to belong to any group, and we have the possibility to create what's called an inline policy, which is a policy that is only attached to a specific user. So that user could or could not belong to a group. You can create inline policies for whichever user you want.

Finally, if Charles and David both belong to the audit team, and you attach a policy to the audit team as well, Charles and David will also inherit that policy from the audit team. In this case, Charles has a policy from the developers' group and a policy from the audit team, while David has a policy from the audit team and a policy from the operations team. This should make a lot of sense when we get into the hands-on part.

![](/img/03/26.png)

**IAM Policies Structure**

Now, in terms of policy structure, you just need to know at a high level how it works and how it is named. This is something you will see frequently in AWS, so get familiar with this structure. It is a JSON document. An inline policy structure consists of a version number, which is usually 2012-10-17—this is the policy language version—an ID, which is used to identify the policy (this is optional), and one or more statements. Each statement has several important parts: the SID is the statement ID, which is an identifier for the statement and is also optional. The effect specifies whether the statement allows or denies access to certain APIs; in the example on the right-hand side, it shows "allow," but it could also be "deny." The principal defines which account, user, or role the policy applies to; in this example, it is applied to the root account of your AWS account. The action is the list of API calls that will be either denied or allowed based on the effect, and the resource is a list of resources to which the actions will be applied. In the example, it is a bucket, but it could be many different things. Lastly, there's a condition that specifies when the statement should be applied or not, but this is optional and not represented in the example.

![](/img/03/27.png)

As you prepare for the exam, make sure you thoroughly understand the effect, principal, action, and resource components. Don't worry; you'll encounter these concepts throughout the course, and you should feel confident with them by the end. That's it for this lecture. I hope you enjoyed it, and I will see you in the next lecture.


**IAM – Password Policy**

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

