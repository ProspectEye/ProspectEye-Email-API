ProspectEye-Email-API
=====================

Description
---------------------
This documentation describes how you can connect ProspectEye to your Email Marketing Solution.

What is ProspectEye?
---------------------
ProspectEye provides extensive data on potential customers visiting your website, giving your sales and market team the upper hand in all stages of your sales processes. 
It enables our costumers to really focus on the most important visitors and take action on the hidden business opportunities related to their company’s market activities; and always be one step ahead of their competitors.

ProspectEye + Email marketing = TRUE
---------------------
To enhance the lead information even more we can add information about visitors converting from a link
sent with an Email Marketing Solution. If the link contains traceable data, we will display personal identified leads in ProspectEye interface. Additional information such as company status, cellphone number, etc. could also be added.
This is a very powerful combination in order to generate hot leads based on email marketing.

Requirements
---------------------
In order to connect your Email Marketing Solution to ProspectEye you need a compatible webservice and the capacity to add data
in the links generated in the email.

The webservice must have the following kind of feature:

``fetchDataBasedOnId(id)``

returns ``String``,``XML`` or ``JSON`` of the information based on the ``id``

Apply for partnership
---------------------
If you are all set on the requirements and would like to connect ProspectEye to your Email Marketing Solution, send us an application email on support@prospecteye.com
with answers to the following questions:

- Existing common clients and your number of existing clients
- Market reach (country specific)
- Your service cost (Yearly basis)
- Yearly revenue

Example on integration setup
---------------------
A link in the email can look like this: http://www.example.com/showcase.php?pedata=M1237632

The data that your Email Marketing Solution should add to every url in the emails is the parameter pedata=M1237632. pedata=M
is the identifier for your solution where M could be any letter. ProspectEye will reserve a letter for you. The rest is an
id (1237632) that is an unique identifier for the information about the email recipient. The information should be collectable
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

- Email is sent from your Email Marketing Solution
- Every link has the added parameter pedata with an identifier
- A recipient clicks on a link in the email and the pedata is sent to ProspectEye
- ProspectEye fetches the data via the Email Marketing Solution webservice with the identifier
- ProspectEye displays the data to enhance the lead

