# Table of Content
- [Table of Content](#table-of-content)
- [Cloud Computing](#cloud-computing)
  - [Key Characteristics (NIST - National Institute of Standards and Technology)](#key-characteristics-nist---national-institute-of-standards-and-technology)
- [Layers](#layers)
  - [IaaS - Infrastructure as a Service](#iaas---infrastructure-as-a-service)
    - [Advantages](#advantages)
    - [Examples](#examples)
  - [PaaS - Platform as a Service](#paas---platform-as-a-service)
    - [Advantages](#advantages-1)
    - [Examples](#examples-1)
  - [SaaS - Software as a Service](#saas---software-as-a-service)
    - [Organizational Forms of Cloud](#organizational-forms-of-cloud)
      - [Private Cloud](#private-cloud)
      - [Public Cloud](#public-cloud)
        - [Exclusive Cloud](#exclusive-cloud)
        - [Open Cloud](#open-cloud)
      - [Hybrid Cloud](#hybrid-cloud)
    - [Advantages](#advantages-2)
    - [Disadvantages](#disadvantages)
- [SaaS - Software as a Service -- General](#saas---software-as-a-service----general)
  - [Comparison of License Models](#comparison-of-license-models)
    - [Traditional Software License Model](#traditional-software-license-model)
    - [SaaS](#saas)
    - [Summary](#summary)
  - [Goal](#goal)
  - [Pricing Models](#pricing-models)
  - [Advantages for the Service Taker](#advantages-for-the-service-taker)
  - [Disadvantages for the Service Taker](#disadvantages-for-the-service-taker)
  - [Advantages for the Service Provider](#advantages-for-the-service-provider)
  - [Disadvantages for Service Provider](#disadvantages-for-service-provider)
  - [Data Protection](#data-protection)
  - [SaaS Companies](#saas-companies)

# Cloud Computing
Cloud Computing is data processing in a "cloud."
It describes the provision of IT infrastructure and IT services as a service over the Internet, with cloud services being accessed on demand and dynamically, and billing based on usage. Offering and usage are done exclusively through technical interfaces and protocols. It encompasses the entire spectrum of information technology and includes infrastructure, platforms, and software. It frees the user from the costly provision, installation, and maintenance of their own computing systems.

## Key Characteristics (NIST - National Institute of Standards and Technology)
- On-Demand Self Service
  - Automatic self-service for users without the provider's intervention.
- Broad Network Access
  - Access from desktops, laptops, and mobile devices via broadband, without being tied to a specific client.
- Resource Pooling
  - Pooling of resources for multiple users.
- Rapid Elasticity
  - Flexible resources that can be quickly reallocated as needed.
- Measured Services
  - Measurable and monitorable services
  - Can be made available to the user as needed.

# Layers 
- Infrastructure
- Platform
- Application

## IaaS - Infrastructure as a Service
IaaS forms the lowest layer in cloud computing, also known as the cloud foundation. Here, IT services such as computing power, storage space, and networks are offered, essentially comprising the basic infrastructure. Users are free to design their own virtual PC clusters, but they are responsible for selecting, installing, operating, and managing the software themselves.

### Advantages
- Scalability, i.e., cloud services can be dynamically adjusted according to usage and demand.
- Example -> Storage space can be expanded or reduced at any time.

### Examples
- GoGrid
- Linode

## PaaS - Platform as a Service
PaaS is a layer above the infrastructure, offering IT services for developing and integrating application software and components. The cloud service provides a programming interface or access to a software environment. In this environment, the developer can create application software and offer it via cloud services. However, the customer does not have access to the underlying layers (OS, hardware).

### Advantages
- No administrative overhead
- Automatic scaling
- Usage-based billing

### Examples
- Microsoft's Windows Azure
- Google's App Engine
- Salesforce.com's force.com

## SaaS - Software as a Service
SaaS represents the top layer.

### Organizational Forms of Cloud

#### Private Cloud
Here, cloud services are provided from an in-house data center. Providers and users know each other and are often within the same company. Additionally, the cloud is controlled and operated within the company itself. Services are only accessible to a limited number of individuals, such as employees and authorized business partners, with access typically via intranet and externally via VPN. Data security issues are almost negligible in this scenario.

#### Public Cloud
Here, cloud services are provided from a publicly accessible system, operated by an external service provider. Since they are public, they can be accessed by any individuals or companies via the Internet. This is no longer limited to internal applications of a single company. However, the user must decide for themselves how many and which data they want to hold outside their immediate control, as public access often leads to data security issues.

Two forms are distinguished:

##### Exclusive Cloud
- Assumes that providers and users know each other.
- Fixed conditions are negotiated, and a contract is signed.
- There are no unknown parties involved.

##### Open Cloud
- Providers and users do not know each other beforehand.
- The provider must develop their offering without direct input from customers and define it in the form of SLAs.
- Due to the multitude of potential users, the entire business transaction and instance usage must be fully automated by the provider.
- Example -> Amazon Web Services

#### Hybrid Cloud
This refers to a scenario where a company operates its own private cloud and additionally uses a public cloud for failover strategies or to handle peak loads.

### Advantages 
- Lower costs, as only usage, not hardware/software, needs to be paid for
- Scalability
- Future-proofing
- Availability
- Location independence
- Simplicity

### Disadvantages
- Mandatory internet access, as data is only available online.
- Data security
- Reliability
- Dependency on the provider
- Insufficient bandwidth
- Loss of control over one's own data

# SaaS - Software as a Service -- General
- Subset of cloud computing.
- Means that software is offered as a service and rented to customers.
- Here, the software (and IT infrastructure) is operated by an external IT service provider and used by the customer as a service.
- The customer only needs an internet-capable PC.
- Access is usually via a web browser.
- These applications are collaboration or industry software required by a company for its business operations or temporary projects.

## Comparison of License Models
### Traditional Software License Model
- Here, the customer receives a license and the right to use the software upon purchase.
- An installation package is provided by the provider.
- Installation requires a complete IT infrastructure (hardware, OS, database, etc.).
- After installation, the software is configured according to business requirements.
- After software deployment, the company takes over the entire operation of the IT infrastructure and IT tasks such as administration, maintenance, etc.
- Unforeseeable follow-up costs usually arise from a maintenance contract associated with the license purchase.
- This includes installing new releases and fixing software errors.

### SaaS
- Here, a service provider provides business or editorial software in a data center.
- They operate it and provide technical support.
- They take over all necessary components of a data center (networks, storage, databases, application servers, web servers, disaster recovery, and backup services).
- Additionally, operational services such as authentication, availability, identity management, production control, patch management, activity monitoring, software upgrades, and customizations are performed.
- The service taker, on the other hand, only needs an internet-capable PC and does not need to install their own software.
- Access is via a web browser.
- For this usage and operation, the service taker pays a user-dependent fee.

### Summary
- Here, it can be said that the IT infrastructure and IT tasks are no longer operated by the service taker but by the service provider.
- The software taker pays not for a software license but for a monthly user-dependent fee.

## Goal
- Reduce investment costs for IT infrastructure (hardware, storage, etc.) and IT tasks (software maintenance, updates, etc.)

## Pricing Models
- Per user per month
  - Payment of a monthly, consistent fee for each registered user who works with the software.
  - Independent of the number of transactions and time, similar to a flat rate.
- Dependent on the scope of functions
  - Extension of the first model
  - Here, too, a monthly consistent fee is paid.
  - However, this is dependent on the scope of functions used.
  - Example -> If there are SRM, CRM, PM, etc., and the service taker only wants to use the CRM, they only need to pay a monthly consistent fee per user for that.
- Transaction-based
  - Billing per transaction made
  - Example -> The service provider is an e-commerce platform where the service taker can sell products. For every generated order in the shop, the service taker pays a percentage of the selling price.
- Freemium
  - Here, the service provider offers a free basic version.
  - This is then supplemented by paid services.
- Others
  - Billing by data volume
  - Billing based on CPU hour usage
  - Constant price over a specific contract period

## Advantages for the Service Taker
- Low investment risk
- Transparent IT costs
- Accelerated implementation
- Reduction of IT process complexity
- Mobility
- Focus on core business

## Disadvantages for the Service Taker
- Dependency on the service provider
- Slow data transfer speeds
- Lower customization options
- Data and transaction security

## Advantages for the Service Provider
- Expansion of IT service offerings
- Additional revenue generation
- Long-term secured revenues
- Better liquidity planning options
- Lower likelihood of software piracy

## Disadvantages for Service Provider
- Investment risk
- Acceptance issues in the IT market
- Possible image damage and revenue losses

## Data Protection
- Customer and employee data are not stored on the customer's own computers but with the service provider.
- According to §11 of the Federal Data Protection Act (Auftragsdatenverarbeitung), the customer is obliged to:
  - Carefully select the provider
  - Conduct regular checks
  - Document the results of the checks
- Additionally, the customer remains responsible for the lawfulness of data processing.
- SaaS contracts must also implement the 10-point catalog of §11 BDSG, as otherwise the customer may face fines of up to 50,000 euros (§43 paragraph 1 No. 2b BDSG)

## SaaS Companies
- Salesforce.com
- NetSuite
- Kenexa
- RightNow Technologies
- Taleo
- Paglo
- athenahealth
- Bazaarvoice
- Jive Software
- Scorpevisio AG
- weclapp GmbH
- salesdoc
- SuccessFactors
