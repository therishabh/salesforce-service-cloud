# [Salesforce Service Cloud](#service-cloud-apex-hours)
## Case Object

A case object typically represents a customer issue or problem, and this object is mainly used by your customer support or your support agents who are constantly in touch with the clients trying to solve their issues.</br>

Support agents can review cases to see how they can deliver better service to their clients</br>

So some of the important details or data that we store in Salesforce for the case objects are accounts. Then we have the comments, which is your service agents comments regarding this case.Then we have the open date and close date, which is basically the date on which the case has been opened and the date on which it has been closed. Then we have contact which is lookup to the contact object (support agent can add the contact who has raised this case.). Then we have the case origin and case status, subject and type.</br>

### Case Closure
By Default in status pick list you'll not see Closed value, we need to enable this closed value from setting.
For that we need to visit setup setting and then type `support setting` then click on Support Setting.
Under this suppor setting page you'll get an option to enable close for status.

![Screenshot 2024-05-24 at 4 27 39 PM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/ca1ddd96-6ef7-480c-a538-7c2ea35327ac)

### Case Queue
Queues allow groups of users to manage a shared workload more effectively. A queue is a location where records can be routed to await processing by a group member.
<img width="1440" alt="Screenshot 2024-05-24 at 7 07 21 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/3366f501-dd33-4ddf-969a-d55e0576251a">

<img width="1440" alt="Screenshot 2024-05-24 at 7 09 44 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e3780c5c-42fa-4103-a11a-b3de0636b4e5">

### Case Assignment
Automatically assign cases to users or queues based on criteria you define. You can create multiple Assignment rules, but only one rule can be active at a time.

From Service Setup, enter `Case Assignment Rules` in the Quick Find box and select Case Assignment Rules
<img width="1440" alt="Screenshot 2024-05-24 at 7 12 15 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/4bc5014a-629a-4fab-b83a-33e5713ac369">
<img width="1440" alt="Screenshot 2024-05-24 at 7 26 10 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e4bdf6eb-d0c0-4fa3-9910-4942befbb6d4">
<img width="1425" alt="Screenshot 2024-05-24 at 7 26 56 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/c9405cfe-d30c-4b8f-b21e-5d82121501fa">
<img width="1440" alt="Screenshot 2024-05-24 at 7 27 18 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/1a08249f-5bf2-40b4-a3a8-b20422976130">

### Case Escalation
Escalation rules automatically escalate case records when a case meets the criteria, which is defined in the case escalation.

<img width="1440" alt="Screenshot 2024-05-24 at 7 37 22 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/1faf637d-1e46-47b7-b426-418a683d2569">

<img width="1440" alt="Screenshot 2024-05-24 at 7 51 05 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/55bc3c58-f021-4b28-8dd4-7102138297f6">

<img width="1440" alt="Screenshot 2024-05-24 at 7 52 00 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/59a45b25-ce67-4015-9da2-5378bfea3f9e">

<img width="1440" alt="Screenshot 2024-05-24 at 7 55 48 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/1a9cb66e-64e7-4a13-b1fa-b6e642b67278">

<img width="1440" alt="Screenshot 2024-05-24 at 7 56 14 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/ecb30a20-2f1c-45e8-8448-5ab19ab03760">

<img width="1440" alt="Screenshot 2024-05-24 at 8 01 39 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/693b73ed-bf3c-4e35-9332-f6d9783514f8">

Test if this Escalation is working or not.
First create a case.
<img width="1440" alt="Screenshot 2024-05-24 at 8 04 07 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/1d9e1718-9186-459f-bd49-24436f3c9e31">

Simply check if this case is been in queue to escalate, we can simply go to our main setup page and search for case escalations in the monitoring section. So basically, if this case, which is on high priority and has the origin as email, it does not get solved or does not get closed within three hours of its creation, then the case will automatically escalate to the next owner.

<img width="1440" alt="Screenshot 2024-05-24 at 8 05 07 PM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/7cd48fda-6592-46a7-abc8-0b85fc696336">

### Assets
Assets can be related to an account, to a contact and to a particular product as well. There are multiple lookup fields in this form. So basically what an asset represents is, for example, if you're running a school business or an educational business and each chair, each sitting chair or each resource that your university has is an asset for you. And to keep track of those assets, you can create records in Salesforce to keep track of them and give them a unique identification.

### Entitlements




### Field Service Object Relationships
To Understand relationships between various Field Service Objects, Go to setup menu and search Schema builder.
In objects, select the following objects :</br>
**Service Appointments**</br>
**Service Resource**</br>
**Service Territory**</br>
**Service territory Member**</br>
You will see the relationship schema of these objects on the canvas.

#### Standard Vs Custom features in the SF projects ?
In Salesforce projects, understanding the difference between standard and custom objects is key to effectively managing data and processes:<br/><br/>
**Standard Objects:**
- Pre-defined by Salesforce: Include core objects such as Accounts, Contacts, Opportunities, Leads, etc.
- Out-of-the-box Functionality: Come with built-in fields, relationships, and business logic.
- Best Practices: Designed according to industry standards, ensuring robust and consistent performance.
- Maintenance and Updates: Automatically updated and maintained by Salesforce with regular releases.
- Quick Setup: Faster to implement as they require minimal configuration.

**Custom Objects:**
- User-defined: Created to address specific business needs that standard objects do not cover.
- Flexible Data Models: Allow custom fields, relationships, and business logic tailored to unique requirements.
- Custom Workflows and Processes: Enable the implementation of complex business processes and automation.
- Scalability: Can be scaled and modified as business needs evolve.
- Integration: Facilitate integration with other systems and applications, enabling seamless data flow.

#### what is cloud ?
Cloud is a specialized software for any industries.

#### What is the difference b/w sales cloud and service cloud in terms of business purpose.
Sales Cloud focuses on sales activities while Service Cloud is designed for case routing automation and speeding up case resolution for support agents.

#### What are the Objects used in service cloud ?
Salesforce Service Cloud objects are database tables that store organization-specific data. Some recommended objects for enterprises include:<br/><br/>
Account, Contact, Case, Case Comment, Case History, Case Team, Email Message, Entitlement, Entitlement Process, Entitlement Template, Knowledge, and Macro.

#### What are the Objects used in sales cloud ?
Sales Cloud comes with standard objects that are included by default. These objects are intended to provide an end-to-end setup for the sales process, and include:<br/><br/>
**Campaigns:** Represents and tracks a marketing campaign, such as a direct mail promotion, webinar, or trade show.<br/>
**Leads:** Potential sales opportunities or new customers<br/>
**Accounts:** Organizations that you do business with<br/>
**Contacts:** Individuals within the accounts<br/>
**Opportunities:** Events or activities for revenue generation<br/>
**Products:** Items, services, or subscriptions that your company sells<br/>
**Price books:** Collections of products and their corresponding prices<br/>
**Price book entries:** Establish the relationship between a product and a price book <br/>

#### what are the objects used in marketing cloud ?
Here are some objects used in Salesforce Marketing Cloud:<br/><br/>

**Journey Builder**<br/>
A tool for mapping and creating customer journeys across email, mobile, advertising, and the web.<br/>

**Custom objects**<br/>
Can be used to personalize messages in Marketing Cloud Connect for Marketing Cloud Engagement.<br/>

**Data extensions**<br/>
Tables that can be used within the relational database in the Marketing Cloud account.<br/>

**Lists**<br/>
Data objects that contain subscriber data.<br/>

**CloudPages**<br/>
A webpage building feature that can be used for Subscription/Preference Centers, or any type of webpage or data capture.<br/>

**Catalog objects**<br/>
Can be defined to appear in the Affinities graph when viewing a unified customer profile. <br/>

#### can we use campaign in the Service Cloud ?
No

#### Difference between lead and opportunity ?
first of all lead is information for a person or a business, lead can be a person also or a company also company means business that will give you some kind of deal. Buy Opportunity is about Opportunity.<br/>
Generally lead is what identified at initial discussion or initial phase, while opportunity is identified at core phase.<br/>
Lead is about non-confirmed business stage, opportunity is about Qualified and confirm stage.<br/>

#### Explain in 1-2 lines, in your own words, the significance of the below Standard objects in salesforce :
1.Campaign<br/>
2.Lead<br/>
3.Account<br/>
4.Contact<br/>
5.Opportunity<br/>
6.Quote<br/>
7.Contract<br/><br/>

**Campaign:** Represents marketing efforts to attract potential customers and track their effectiveness.<br/>
**Lead:** Captures information about potential customers who have shown interest in your products or services.<br/>
**Account:** Stores information about companies or organizations you do business with.<br/>
**Contact:** Holds details about individuals associated with accounts.<br/>
**Opportunity:** Tracks potential sales and revenue-generating deals.<br/>
**Quote:** Documents the proposed prices of products or services for a particular opportunity.<br/>
**Contract:** Manages the terms and agreements between your company and its customers.<br/>

---------------------------------------------------------
---------------------------------------------------------
---------------------------------------------------------
---------------------------------------------------------
---------------------------------------------------------
# Service Cloud (Apex Hours)
---------------------------------------------------------
---------------------------------------------------------
---------------------------------------------------------
---------------------------------------------------------

<img width="1424" alt="Screenshot 2024-06-11 at 5 04 23 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/a7bcc47d-7fcb-45b8-9679-9f4c4da7dddc">
<br/><br/>
<img width="1422" alt="Screenshot 2024-06-11 at 5 05 12 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e2248144-d77d-46a0-bfd8-536a3ded9828">
<br/><br/>
<img width="1434" alt="Screenshot 2024-06-11 at 5 07 25 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/c9376886-afd5-4d30-8cdc-c1d631ef1a69">
<br/><br/>
<img width="1437" alt="Screenshot 2024-06-11 at 5 08 50 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e25dc064-6cca-402d-88e1-2464782b7dd0">
<br/><br/>
<img width="1431" alt="Screenshot 2024-06-11 at 5 09 54 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/d12c9a0e-b370-4467-84e0-c77653499844">
<br/><br/>
<img width="1434" alt="Screenshot 2024-06-11 at 5 10 22 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/5d28ce2c-e1a3-42fb-aed6-40930c2ffd41">
<br/><br/>
<img width="1434" alt="Screenshot 2024-06-11 at 5 26 12 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/a9703b29-1f8c-4e45-8ecc-42e0e12f6489">
<br/><br/>
<br/><br
       
### Demo

##### Create a user profile for customer support
![Screenshot 2024-06-11 at 5 42 29 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/de42c5b1-11e3-461e-93bc-b3ce943326c2)

##### Create a new app
![Screenshot 2024-06-11 at 5 46 06 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/3f8d19f2-59e1-48aa-93ec-1f2fc2cac00e)
<br/><br/>
![Screenshot 2024-06-11 at 5 50 56 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/eb806825-b84c-40ab-92eb-ffc243d00da0)
<br/><br/>
![Screenshot 2024-06-11 at 5 54 00 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/be172844-5ff1-4df4-be9c-66dc8cbf6cac)
<br/><br/>
![Screenshot 2024-06-11 at 5 54 13 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/7db7b695-c86e-442f-9bc7-8b1d1a34728a)
<br/><br/>
![Screenshot 2024-06-11 at 5 54 59 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e1edb918-6e92-480d-8880-17bacfb65970)


## Basic Setup
<img width="1433" alt="Screenshot 2024-06-11 at 6 12 05 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/9f80aa49-b6d3-409d-bd5d-9d69029e893c">


#### Customize Support Setting
![Screenshot 2024-06-11 at 6 13 06 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/8fc71be3-ddbf-4f62-b7a0-fa4e64ca904b)

#### Set Business Hours
<img width="1438" alt="Screenshot 2024-06-11 at 6 13 59 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/b5ffbbce-a3a1-4e27-bf72-8b97fea831d4">

![Screenshot 2024-06-11 at 6 16 34 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/a3a0954a-1cbf-4261-9bc5-11a72c9db1a4)

#### Set up Support Holidays
<img width="1438" alt="Screenshot 2024-06-11 at 6 17 04 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/b84d24a8-2a13-4309-a515-e79a55901f67">
<img width="1438" alt="Screenshot 2024-06-11 at 6 17 04 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/84da3d2b-dd5c-40b0-9b9d-311fde32b0ad">
<img width="1438" alt="Screenshot 2024-06-11 at 6 17 04 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/e9f97a8e-2b95-4bad-942d-43c957e2b581">
<img width="1438" alt="Screenshot 2024-06-11 at 6 17 04 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/a6574681-fe43-43a4-a87e-2df82868df40">


### Case Creation:

#### Manual creation
// do it manually by click on add new button

#### Email to Case
<img width="1438" alt="Screenshot 2024-06-11 at 7 24 26 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/ed3ed215-d1dc-41a4-982c-f98dc89b4587">

<img width="1438" alt="Screenshot 2024-06-11 at 7 25 41 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/41bb06e7-815a-4dcf-9d9e-7837784d8093">

![Screenshot 2024-06-11 at 7 28 46 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/02711e24-18af-4993-97e5-ea624a46cf81)

![Screenshot 2024-06-11 at 7 29 28 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/29600c59-2765-4a24-a4b7-d3c0d0fdda92)

#### Web to case
<img width="1437" alt="Screenshot 2024-06-11 at 7 34 10 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/b29d701a-d313-43d5-9ff3-55dc51b9428c">

<img width="1437" alt="Screenshot 2024-06-11 at 7 34 10 AM" src="https://github.com/therishabh/salesforce-service-cloud/assets/7955435/f8709e12-2270-4123-b6f0-5df6a68424eb">

![Screenshot 2024-06-11 at 7 39 59 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/89e44d86-25c3-435a-b2a5-5faa844f1064)


![Screenshot 2024-06-11 at 7 40 20 AM](https://github.com/therishabh/salesforce-service-cloud/assets/7955435/15765e32-a1d9-4555-a6ac-20ee71b56c17)








