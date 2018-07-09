## Welcome to the SeazMe Platform

We designed SeazMe to facilitate collaboration, findability, and communication in the corporate world. 

SeazMe was created as a Platform to be very modular.   We found when Open Sourcing this was crucial for other corporation to also be able to create their versions.  We have found that in the corporate environment - the easier it was to break into pieces the easier it was to collaborate on with each team being able to clearly report what they had worked on. 

The first crucial piece is [the DataHub](https://github.com/paypal/seazme-hub).   The DataHub was designed for all the datasources to be crowd sourced within the company.  The Data is kept in Hbase for its concurrency and consistency.  It has an API that is kept in a DMZ zone to make it easy for not only different departments and offices but also for acquisitions.   It creates a centralization point.   If a team wants to share data from a datasource like Confluence, GitHub, Rally, JIRA, an internal website or even API documentation all they have to do is [connect to the API](https://github.com/paypal/seazme-sources).  The team determines their SLA for keeping the data up to date and publishes it. 

Secondly, We are creating an API to work with Gimel.  [Gimel is an open source adaption of Juypter Notebooks](https://github.com/paypal/gimel).  This allows our teams to do analytics on top of the DataSources that are being gathered in DataHub. 

Thirdly, we are realizing the Universal Search components.  We have divided this up.  We have setup QA and Production Elastic Search Clusters.  We are working on API's to make it easy for tools to be able to use our search results in their tools.  We also pull data from the Hbase clusters to create the Elastic Datasets.  We feedback metadata from Elastic Search to the DataHub Hbase clusters for backup and so we can rebuild Elastic clusters regularly.  [We also have a global search interface](https://github.com/paypal/seazme-search) so that employees can choose what datasources they want to search and can if they choose - search them all. 

## Coming Soon!

A Chrome plugin so that users could give feedback on search results AFTER the clicked thru.

Doc2Doc - that will allow technical writers to search for a paragraph or fact that is changed and find any other uses of that and email all the owners asking them to update the "fact."

Special Security tools for the DataHub that look for accidental security violations like including UserName and password in documentation. 

A Profile Page that includes personalized search results. 

Clover++ - which allows corporate users to add groomed links. 

> Written with [StackEdit](https://stackedit.io/).
