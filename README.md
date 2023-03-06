# AWS---Certificate
Plural Course

1. Cloud - Introduction to cloud computing: SaaS, PaaS, and IaaS.

2. Services - This includes the following services:

        Computing and data processing (EC2, Lambda) to manage virtual machines and event-driven computation
        File Storage (S3) to store and access objects efficiently
        Networking (VPC, Route 53) to configure networks and routing
        Database to store SQL (RDS) and NoSQL (DynamoDB, SimpleDB) data
        Notification (SNS) services for portable devices like cell phones
        Message (SQS) storage and transfer service for communication and process management
        Others: Time Sync for accurate current time and CloudFormation to automate work, etc.
3. Security - 

        Shared Security Model, Compliance and Artifact, Web Application Firewall(WAF), Inspector, Trust Advisor, CloudTrail, Cloud Watch, Identity and Access Management (IAM) services
        
4. Billing - The pricing and billing structure of different services as per usage, quota, and plans



# 1. Cloud - same with Azure

1.1 Concepts/ Computing models:

          On Premises: customer do all the things - include the infrastrauctures.
  
          IaaS provides access to resources such as virtual machines and virtual storage: Google compute engine
                infrastructure = actual servers
                scaling is fast; X own hardware
                pay-as-you-go
                agile
                No CapEx no upfront costs
                Consumption-based model(OpEx)
                allows to deploy [VMs + Networks + Physical Buildings + storage] in a cloud
          PaaS provides execution environments, application development, and deployment tools: Azure, AWS
                supports web application life cycle
                avoid license hell
                develop apps by themselves
                don't maintain/update the infrastructure
                No CapEx no upfront costs
                Extra agile
                less hardware and software skills needed
                Consumption-based model(OpEx)
                [IaaS + Middleware + Tools] deploy Web servers, database and development tools in a cloud
          SaaS provides software as a service to end-users: Google, Salesforce
                Providing a managed service
                pay an access fee to use/ pay-as-you-go
                No CapEx no upfront costs
                agile
                no maintenance and latest features
                software stored in a central location and customers access via subscription basis
                [PaaS + Apps] allows to run apps in cloud e.g Office 365
          FaaS Function as a server
                uses a service-hosted remote procedure call.
          DSaaS - data/ analytics
          NaaS - network transport connectivity
          Serverless 
                Azure is an instance of this
                Extreme PaaS
                deliver exact units of recources.
         [PaaS - extreme] - allocates the extract amount of application needs.


1.2 Cloud Architecture Models/ Delpoy Model:

          Private - resources exclusively owned, managed by single organization
                Pros:
                      scalability and efficiency
                      security           
                Cons:
                      Maintenance
                      Staffing
          Public -- Azure, AWS, GCP - owned, managed by vendor alone
                Pros:
                      No purchase/maintenance of hardware and software
                      only pays for the services that they consume/ pay-as-you-go
                      Lcost-effective reliability
                      scalability is unlimited
                      high reliability - a vast network of servers ensures against failure
                Cons:
                      No control over features and version
                      No physical access
          Hybrid     
                Pros:
                      Avoid disruptions and outages
                      Adhere to regulation, governance
                      Span both public and private cloud
                      Alleviate CapEx - pay for extra computing power only when needed
                      scalibility
                      flexibility
                      control
                      ease
                Cons:
                      Complex infrastructure
          Community - collaborative effort between multiple organiaztions. Multiple organizations are working on joint projects
                Pros:
                Cons:

1.3 Global Infrastructure

        AWS Regions
                
                represents a cluster of data centers in a specific geographic location.
                
        AWS Availability Zones
        
                Consists of one or more data centers.
                Multiple availability zones are included in each region.
                Located in the geographic location of regions.(96)
                Enable high-availability
           
        [Naming of Region and Availability Zones]
                
                us-east-2a
                area-subarea-number
                us-east-2       =       region
                us-east-2a      =       availability zones
        
        AWS Local Zones
        
                Each is an extension of an AWS Region.
                Place compute, storage, database, and other select AWS services closer to end-users. 
             (AWS Wavelength Zones)
                AWS infrastructure deployments that embed AWS compute and storage services within communications service providers’ (CSP) 5G networks.
        
        AWS Edge Locations - 边缘位置
        
                Designed to deliver services with the lowest latency possible. 
                Serve content where it is closest to end users
                [CDN: Content Delivery Network]
                CloudFront, cache copies of the content that it serves, so the content is closer to users and can be delivered to them faster.缓存其所服务内容的副本，因此内容更接近用户并且可更快地交付
                Route 53, which serves DNS responses from edge locations, so that DNS queries that originate nearby can resolve faster (and, contrary to what you might think, is also Amazon’s premier database).
                为来自边缘位置的 DNS 响应提供服务，因此来自附近的 DNS 查询可以更快地解析（它也是亚马逊的首要数据库）
                Web Application Firewall and AWS Shield, which filter traffic in edge locations to stop unwanted traffic as soon as possible. 过滤边缘位置的流量以尽快阻止不需要的流量。
        
1.4 Cloud Economics

        CapEx = Capitalized Expenditure
               One-time expenditure to buy tangible/fixed assets, such as building the data center
               needs upfront costs: buildings, servers, supporting equipment
        OpEx  = Operational Expenditure 
               Ongoing expenses incurred on services and products. 
               Pay-as-you-go. How much you use.
               No up-front investment
               Capacity scales to meet user demand immediately              
        TCO = Total Cost of Ownership 总拥有成本
        
        AWS Cost Planning Tools
                - AWS Pricing Calculator: in-depth analysis of the cost
                - AWS Migration Hub: [transitioning] for Business Case 工作负载到云端提供建议
        AWS Resource Tags
                - Tags can be used in AWS Costs Explorer to see separate items
                - Cost allocation report includes costs grouped by active tags.
        AWS Organizations
                Allows multiple accounts, billing
        
        Build a Business Case: tools = [ AWS Migration Hub ] && [ Migration Evaluator ]
                - Analyze the current workloads
                - Forecast infrastructure needs
                - Create a TCO analysis of both options
        AWS Pricing Calculator - like linode deployment
        
        [ AWS Costs Explorer ] = a user interface for reviewing AWS costs, forecasting future costs, and providing recommendations for cost optimization.
        [ AWS Migration Hub ] + [ AWS Migration Evaluator ] = creating a business case to move to the cloud.
        
1.5 Supporting AWS Infrastructure

        AWS [ Personal Health Dashboard ] provides alerts and remediation guidance when AWS is experiencing events that may impact you.” 
        AWS [ Trusted Advisor ] is an automated tool for checking your AWS usage against best practices.
         
        AWS Trusted Advisor provides recommendations in the following five categories:
                1. Cost Optimization
                2. Performance
                3. Security
                4. Fault Tolerance
                5. Service Limits
                
        Support Plan Tiers   
                Support Plan     Email      Chat       Phone
                
                Basic            
                Developer        YES
                Business         YES        YES        YES
                Enterprise       YES        YES        YES

        Support Plan Tiers   
                Incident Type    Developer   Business  Enterprise
                
                Genaral 
                Guidance           24h          24       24 
                
                System
                Impaired                        12       12
                
                Production
                System Impaired                  4        4
                
                Production
                System Down                      1        1
                 
                Business Critical
                System Down                             15 minutes
       
# 2. AWS Core Services

        2.1 Interacting with AWS
        
                Console
                CLI: Command Line Interface
                SDK: Software Development Kit
        
        2.2 Compute Services -- IMPOERTANT
        
                2.2.1 Amazon EC2 = Amazon Elastic Compute Cloud
                
                        A web service that provides secure, resizable compute capacity in the cloud.Service that provides secure and resizable virtual servers
                        Needs to know the [Instance Types] + [Root Device Type] + [Amazon Machine Image (AMI)] + [Purchase Option]
                        [Instance Type]: processor, memory & storage type
                        [Root Device] Instance Store & Elastic Block Store
                        [AMI] 
                        [Purchase Options] 
                                On Demand - Pay by the second for the instance that ara launched
                                Reserved - Purchase in advance for 1-3 year. A capacity reservation for the selected instance type.
                                Savings Plan - Commit to a level of usage for EC2, Fargate, or Lambda for a 1 or 3 year period at a discount. Does not reserve capacity.
                                Spot - leverage unused EC2 capacity in a region for a large discount.
                                Dedicated - 
                                
                                
                2.2.2 AWS Elastic Beanstalk
                
                        A Platform (PaaS) for scaling and deploying web apps and services across a specific list of technologies

                2.2.3 AWS Lambda
                
        2.3 Content and Net work Delivery
        
        2.4 File Storage Services





                
                

