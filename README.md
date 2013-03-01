ProspectEye-Email-API
=====================

Description
---------------------
This documentation describes how you can connect ProspectEye with your Email Marketing solution.

What is ProspectEye?
---------------------
ProspectEye is a tool that collects leads based on the traffic on your webbsite. Every visitor can be a potential
customer and ProspectEye helps you filter out the the hottest leads from you visitors.

ProspectEye + Email marketing = TRUE
---------------------
To enhance the lead information even more we can add another dimension to visitors that choose to convert by clicking on a link
sent from an email marketing solution. If the link contains traceable data, leads shown in ProspectEye can then contain information like email, company, name, etc.
This is a very powerful combination in order to generate hot leads based on email marketing.

Requirements
---------------------
In order to connect your email marketing solution to ProspectEye you need a compatable webservice and the capacity to add data
in the links generated i the email.

The webservice must have the following feature:

``fetchDataBasedOnId(id)``

returns ``String``,``XML`` or ``JSON`` of the information based on the ``id``

Apply for partnership
---------------------
If you have the requirements and would like to connect ProspectEye with you Email marketing solution. Send an email to support@prospecteye.com
with answers to the following questions:

- Existing common clients
- Market reach (global or country specific), your number of existing clients
- Your service cost (Yearly basis)
- Yearly revenue

Example
---------------------
A link in the email can look like this: http://www.example.com/showcase.php?pedata=M1237632

The data that the email marketing solution should add to every url in the emails is the parameter pedata=M1237632. pedata=M
is the identifier for your solution where M could be any letter. ProspectEye will reserv a letter for you. The rest is an
id (1237632) that is an unique identifier for the information about the email reviever. The information should be collectable
via a webservice where the url-id is the identifier to fetch the data.

The fetchable data could be represented as a string

``
email=firstname.lastname@example.com|subject=example email|campaign=example campaign
``

or JSON

```
{
  email: 'firstname.lastname@example.com',
  subject: 'example email',
  campaign: 'example campaign'
}
```

The follow procedure is praxis:

- Email is sent from Email Marketing solution
- Every link has the added parameter pedata with and identifier
- A person clicks on the link and the pedata is sent to ProspectEye
- ProspectEye fetches the data via the email marketing solutions webservice with the identifier
- ProspectEye shows this data to enhance the lead

