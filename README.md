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


