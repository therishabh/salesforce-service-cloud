# salesforce-service-cloud
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
In Salesforce projects, understanding the difference between standard and custom objects is key to effectively managing data and processes:
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

#### How to use Standard features of Salesforce in projects?

#### what is cloud ?
Cloud is a specialized software for any industries.

#### What is the difference b/w sales cloud and service cloud in terms of business purpose.
Sales Cloud focuses on sales activities while Service Cloud is designed for case routing automation and speeding up case resolution for support agents.

#### What are the Objects used in service cloud ?
Salesforce Service Cloud objects are database tables that store organization-specific data. Some recommended objects for enterprises include:
Account, Contact, Case, Case Comment, Case History, Case Team, Email Message, Entitlement, Entitlement Process, Entitlement Template, Knowledge, and Macro.

#### What are the Objects used in sales cloud ?
Sales Cloud comes with standard objects that are included by default. These objects are intended to provide an end-to-end setup for the sales process, and include:
Campaigns: Represents and tracks a marketing campaign, such as a direct mail promotion, webinar, or trade show.
Leads: Potential sales opportunities or new customers
Accounts: Organizations that you do business with
Contacts: Individuals within the accounts
Opportunities: Events or activities for revenue generation
Products: Items, services, or subscriptions that your company sells
Price books: Collections of products and their corresponding prices
Price book entries: Establish the relationship between a product and a price book 

#### what are the objects used in marketing cloud ?
Here are some objects used in Salesforce Marketing Cloud:

Journey Builder
A tool for mapping and creating customer journeys across email, mobile, advertising, and the web.

Custom objects
Can be used to personalize messages in Marketing Cloud Connect for Marketing Cloud Engagement.

Data extensions
Tables that can be used within the relational database in the Marketing Cloud account.

Lists
Data objects that contain subscriber data.

CloudPages
A webpage building feature that can be used for Subscription/Preference Centers, or any type of webpage or data capture.

Catalog objects
Can be defined to appear in the Affinities graph when viewing a unified customer profile. 

#### can we use campaign in the Service Cloud ?
No

#### Difference between lead and opportunity ?
first of all lead is information for a person or a business, lead can be a person also or a company also company means business that will give you some kind of deal. Buy Opportunity is about Opportunity.
Generally lead is what identified at initial discussion or initial phase, while opportunity is identified at core phase.
Lead is about non-confirmed business stage, opportunity is about Qualified and confirm stage.

#### Explain in 1-2 lines, in your own words, the significance of the below Standard objects in salesforce :
1.Campaign
2.Lead
3.Account
4.Contact
5.Opportunity
6.Quote
7.Contract

**Campaign:** Represents marketing efforts to attract potential customers and track their effectiveness.
**Lead:** Captures information about potential customers who have shown interest in your products or services.
**Account:** Stores information about companies or organizations you do business with.
**Contact:** Holds details about individuals associated with accounts.
**Opportunity:** Tracks potential sales and revenue-generating deals.
**Quote:** Documents the proposed prices of products or services for a particular opportunity.
**Contract:** Manages the terms and agreements between your company and its customers.


























