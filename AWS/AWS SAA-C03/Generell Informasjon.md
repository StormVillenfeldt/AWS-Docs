Generell informasjon
	Private Cloud
	Public Cloud
	Hybrid Cloud

Types of service
	IaaS
	SaaS
	PaaS
	On Prem

Why choose AWS?
- Cheap if the company is small
- Easier to scale
- Flexible, Efficient & Smart stragety wise
- CapEx, OpEx
- Upscale: Create a bigger server to host more tasks
- Outscale: Create more server to host more tasks


Why avoid cloud?
- Depending on project, there is a good possibility that cloud services are not any cheaper than using in-house datacenters


About AWS:
- 273 Services to choose from as of 07.08.2023
- Owns 33% of the global market share for cloud computing
- Opens up for global infrastructure, something other services are not as profficient in
- 2-3 Availability zones

- Availability Zone: A regional sub-section of zones, ex: eu-central-1 (Frankfurt) as three AZ's; eu-central-1a, eu-central-1b, eu-central-1c
- Always 2 AZ's, most of the time there are 3
- Client can choose to only utilize 1 AZ

- Edge locations are even more specific points compared to AZ's. A customer in Norway would like to atleast store cache on the closest edgepoint, and perhaps the rest of the data on a database on eu-central-1
- A low-latency app would require a edge location, otherwise it would be too slow and no customer would like to use it


Services:
- EC2 instances (Virtual Machines) are region locked, meaning that a machine running on eu-central-1 is not available for config on eu-central-2
- Globally scoped services are services that are not region locked, they can be access from any region at any time. Ex: ACM, IAM
- Amazon Route 53 is the DNS tool most frequently used on AWS
- AWS is the only major cloud platform that is API-first
- As with most other cloud platforms, security is of high priority


Shared Responsibility Model:
- The Shared Responsibility Model (SRM) is a model describing which parts of the services selected that the client is responsible for, and which AWS is responsible for. This is almost always a trade-off situation, where the client has to choose between flexibility and more customization, or simplicity. There is no answer to which is better, and this is more often than not completely dependet on the customer. App-developers who only wants to focus on creating an app and making it available would like to avoid being responsible for things such as security, connectivity and storage. However, a major tech company would probably want to be much more in control of every single alternative, and build their own tools based on AWS services.
- ![[Pasted image 20230809082237.png]]

Availability Zones:
- AZ's demand their very own subnet of the original subnet, meaning that if a client uses all 3 AZ's that would mean 3 distinct subnets. 10.2.0.1, 10.3.0.1, 10.4.0.01 for example
- AZ's are account spesific, meaning that if another user would like to access a application beloning to someone else, they would have to reference the ID of that spesific AZ