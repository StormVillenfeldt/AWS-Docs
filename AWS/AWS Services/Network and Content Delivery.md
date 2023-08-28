#### List of services
	- Amazon API Gateway
	- Amazon CloudFront
	- Amazon Route53
	- Amazon Virtual Private Cloud
	- AWS App Mesh
	- AWS Cloud Map
	- AWS Direct Connect
	- AWS Global Accelerator
	- AWS Private 5g
	- AWS PrivateLink
	- AWS Transit Gateway
	- AWS Verified Access
	- AWS VPN
	- Elastic Load Balancing

#### Amazon API Gateway <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### Amazon CloudFront <mark style="background: #D2B3FFA6;">Not Started</mark>

#### Amazon Route53 <mark style="background: #D2B3FFA6;">Not Started</mark>

#### Amazon Virtual Private Cloud (VPC) <mark style="background: #FFB86CA6;">Incomplete</mark>
A Virtual Private Cloud is a service on AWS that allows the user to create their own private network environment. Multiple VPCs can be used by a singular app, for example, it is common for databases to be on their own VPC. Every VPC has to have their own subnet, as with the AZ's. VPCs are access through either IPv4, IPv6 or both. Flow logs contain the logs and history of activity on the VPC. 

For security the user can use Security Groups and/or Network ACL. Security Groups exist on instance level. 
![[Pasted image 20230809082359.png]]
Each NACL requires its own subnet. Security Groups has a pre-existing deny rule on creation, wheras NACL has to be defined to both allow and deny traffic. NACL is stateless, and Security Groups are statefull. 

Internet Connectivity
- Internet Gateway is a component of VPC
- Only public ip-adresses are allowed through an internet gateway
- Dependent on Security Group or NACL
NAT Gateway
- NAT Gateway is a tool used translate IP-adresses
-  NAT Gateway allows for the possibility of traffic from a private adress, through a public adress
- The gateway is installed on a public address, and requires a routing table to be able to transmit traffic to the internet gateway
- NAT Gateways operate on the AZ level

#### AWS App Mesh <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### AWS Cloud Map <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### AWS Direct Connect <mark style="background: #D2B3FFA6;">Not Started</mark>

#### AWS Global Accelerator <mark style="background: #D2B3FFA6;">Not Started</mark>

#### AWS Private 5G <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### AWS PrivateLink <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### AWS Transit Gateway <mark style="background: #FFB86CA6;">Incomplete</mark>
Transit Gateways allow for VPC's to talk to eachother through automatic config. Normally this has to be setup both ways before communication is possible, but Transit Gateway makes it easy to setup many VPC's that can communicate

#### AWS Verified Access <mark style="background: #FF5582A6;">Out Of Scope</mark>

#### AWS Client VPN <mark style="background: #D2B3FFA6;">Not Started</mark>

#### AWS Site-To-Site VPN <mark style="background: #D2B3FFA6;">Not Started</mark>

#### Elastic Load Balancing (ELB) <mark style="background: #D2B3FFA6;">Not Started</mark>







AWS Services:
- Compute
	- AWS Batch
	- AWS Elastic Beanstalk
	- Vmware cloud on AWS
	- AWS Wavelength
	- AWS Serverless Application Repository
	- AWS Outpost
	- Amazon Elastic Compute Cloud (EC2)
	- AWS Compute Optimizer

- Serverless
	- AWS Fargate
	- AWS Lambda
	- AWS AppSync

- Containers
	- AWS Elastic Kubernetes Serivce (EKS)
	- AWS Elastic Container Service (ECS)
	- AWS Elastic Container Registry (ECR)
	- AWS ECS Anywhere

- Databases
	- AWS Aurora
	- AWS DocumentDB
	- AWS DynamoDB
	- AWS Keyspaces
	- AWS Database Migration Service (DMS)
	- AWS Neptune
	- AWS TimeStream
	- AWS Relational Database Service (RDS)
	- AWS ElastiCache
	- AWS Quantum Ledger Database (QLDB)

- Machine Learning
	- AWS Comprehend
	- AWS Forecast
	- AWS Lex
	- AWS Polly
	- AWS Rekognition
	- AWS SageMaker
	- AWS SageMaker Ground Truth
	- AWS Textract
	- AWS Transcribe
	- AWS Translate
	- AWS Fraud Detector
	- AWS Kendra

- Developer Tools
	- AWS X-Ray

- Front-end Web and Mobile
	- AWS Amplify
	- AWS Device Farm

- Network and Content Delivery
	- AWS Transit Gateway
	- AWS CloudFront
	- Amazon Route 53
	- AWS Direct Connect
	- AWS Global Accelerator
	- AWS Client VPN
	- AWS Site-To-Site VPN
	- AWS Elastic Load Balancer (ELB)
	- AWS PrivateLink

- Storage
	- Amazon Elastic Block Store (EBS)
		- Tilsvarende harddisk
		- Tilkobles EC2 instanser
	- AWS Storage
	- Amazon Elastic File System (EFS)
		- Filsystem
	- Amazon Simple Storage System (S3)
		- Flatt filsystem
		- Kan programatisk hente filer
		- Ingen mapper, alt ligger på samme plass
		- Utrolig raskt
		- Ubegrenset lagring
		- Get/Post API-kall for access
		- S3 Standard
		- S3 Glacier
			- Treig, men bra for gamel og mindre brukte filer
			- Fungerer som et arkiv
		- S3 Intelligent Tiering
		- Eksempel på en tradisjonell S3 pipeline:
			- S3 Standard for nye filer
			- 30dager: S3 Infrequent Access
			- 180dager: S3 Glacier
			- Etter mye lengre tid: Enten slett eller S3 Glacier Deep Archive
	- AWS Snowball Edge
		- Portable, no connection needed, compute power
	- AWS Snowball
		- Minste mulige eksterne fysiske lagringsenhet
		- ~ 10tb
		- Ekstremt mobil, kan ha med flere da de er lett å lagre
	- AWS Snowcone
		- Medium alternativ for ekstern fysisk lagring
		- Som med snowball så fungerer snowcone uten kobling til nett, da den er programmert på forhånd før den tas i bruk
		- Kan lagre betydelig mye mer data enn Snowball, petabytes
		- Vanlige bruksområder vil være; Oljerig, Fiskebåter, Isolerte datasentre
	- AWS Snowmobile
		- Stor fysisk lastebil som frakter tradisjonelle harddisker
		- Billigste måte å lagre/sende gigantiske mengder data
		- Brukes bare av enorme firma som håndterer unormale mengder data, som store banker eller datafarmer
	- AWS Storage Gateway
		- Hvis en kunde vil ha on prem access men bare på cloud
		- Migreringsverktøy, men tillater fortsatt on prem access
	- AWS Elastic Disaster Recovery (EDR)
		- Data tapt
		- Point in time recovery
		- Disaster planning etc
	- Amazon FSx
		- Filsystem
		- Likt EFS, men for windows workloads
		- Lustre
		- Windows
		- NetAPP ONTAP
		- OpenZFS
		- Hvis gitt spørsmål om win/lustre/NetAPP/ZFS -> Svaret er FSx
	- AWS Backup
		- Backup tjeneste

- Migration and Transfer
	- AWS Application Discovery Service
		- Agentless Discovery
	- AWS Transfer Family
		- Enklere å migrere filer
	- AWS DataSync
		- Agent
		- Mellom On Prem og AWS
	- AWS Migration Hub
		- Tracke migrering
		- Oversikt
	- AWS Application Migration Service
		- Gir automatisert lift and shift plan

- Media and Services
	- Amazon Elastic Transcoder
		- Klargjør flere kvaliteter av videoer
		- Transcoder filer til ønsket oppløsning
	- Amazon Kinesis Video Streams
		- Streaming
		- Integrere videofiler m/ andre tjenester
		- F.eks du har en app som ska kunne ha streaming funksjonalitet

- Security, Identity & Compliance
	- Amazon Cognito
		- Mulig for sign in på applikasjoner
	- Amazon GuardDuty
		- Fundamental tjeneste
		- Overvåker AWS konto, alt
		- Rapporterer
	- Amazon Inspector
		- Issus på apps
		- Finner de
		- Leter etter best practise i kundes tjenesteweb
	- Amazon Macie
		- ML og AI
		- Beskytter sensitiv info
		- Forhindrer incidents
	- AWS Artifact
		- Security Comp. Reports
	- AWS Certificate Manager (ACM)
		- Sertifikater
	- AWS CloudHSM
		- Kryptografisk modul
		- Høy sikkerhet, som helse/finans
		- Kryptering på cloud
	- AWS Directory Service
		- Manager tjeneste
		- Lar deg koble til windows active directory
	- AWS Firewall Manager
		- Managed Firewall i AWS
		- Automatisert, mange firewalls
	- AWS IAM
		- Mye brukt, setter tilganger og roller på brukere
		- Essential tool i AWS
	- AWS Key Management Service (KMS)
		- Tjeneste som åpner for bruk av kryptografiske nøkler
	- AWS Secrets Manager
		- Passord manager
	- AWS Security Hub
		- Hub for alt sikkerhetsrelatert
	- AWS Shield
		- DDOS Protection
		- Default active tjeneste
		- Shield Advanced er en dyrere mer avansert versjon
			- Regninger relatert til DDOS går direkte til AWS hvis shit hits the fan, men tjenesten i seg selv koster sånn 40k usd i mnd
	- AWS WAF
		- Web firewall for API
		- Fungerer bra mot de mest kjente formene for angrep
		- Script angrep eller SQL injections
	- Amazon Detective
		- Analyserer root cause
		- Brukes som et verktøy for å finne gjentagende problemer
	- AWS Resource Access Manager
		- Dele AWS på tvers av konto
	- AWS Audit Manager
		- Audits og compliance
	- AWS Network Firewall
		- Brannmur

- Management and Governance
	- Amazon CloudWatch
		- Logger & Matrise generte ting kan sees på
	- AWS Auto Scaling
		- Auto scale EC2 instanser
	- AWS CloudFormation
		- Infrastructure as Code
		- Deploy ressurser
	- AWS Config
		- Audit
	- AWS License Manager
		- Lisenser
	- AWS Health Dashboard
		- Viser helsen til alle AWS tjenester
	- AWS Management Console
	- AWS CloudTrail
		- Logger API kall
		- Hvem og når
	- AWS Service Catalog
		- Dele med andre teams etc
		- Hyllevare
	- AWS Systems Manager
		- Mye legacy på EC2 som må passes på, bruk denne
	- AWS Trusted Advisor
		- Gir anbefalinger på alt
	- AWS Well Architected Tool
		- Pinpoint punkter for forbedring
	- AWS ControlTower
		- Manage kontoer, bruk denne
	- AWS Organizations
		- Organiserer kontoer
		- Organization Units, inhert from group
	- AWS Proton
		- Fully Managed
		- Infrastructure provisioning
	- AWS Fault Injection Simulator
		- Teste og simulere feil
	- Amazon Managed Grafana
		- Grafana support på Amazon, bare fully managed
	- Amazon Managed Service for Prometheus
		- Kubernetes
		- Fully managed for Prometheus
	- AWS Distro for OpenTelemetry
		- Distro for OpenTelemetry prosjekter
		- Telemetry ut av app

- Cloud Financial Management
	- AWS Budgett
		- Hjelp med å sette opp budsjetter
	- AWS Cost and Usage Report
		- Hvordan pengene er brukt
	- AWS Cost Explorer
		- Utforske kostnader
	- Savings Plan
		- Prismodell for planlegging
		- Reservere for senere
		- Mulighet for å spare