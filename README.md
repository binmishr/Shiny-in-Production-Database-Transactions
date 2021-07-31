# Shiny-in-Production-Database-Transactions

An important aspect of maintaining databases with an application interface is to ensure atomicity. When performing multiple writes on a database, any failures that occur during the operations should not violate any logical rules. The most common analogy is a financial transaction. If person A withdraws X dollars from their account and deposits into the account of person B then the withdrawal and deposit should occur as a whole transaction. If only one occurs, you have either created or deleted currency (your government does not approve of this). The DBI package provides a couple of abstractions to perform transactions with R and seamlessly implement them into a shiny application.

The following demonstrates maintaining atomicity through an application that allows the user to re-allocate resources to 4 containers. Any container can transfer resources to another container but the amount must be greater than 0 and less than what is currently in the container that is losing resources. The condition that should always be met is that the sum of the resources should equal 100. 

The details of the codeset and plots are included in the .pdf file and attached in this repository to follow.
