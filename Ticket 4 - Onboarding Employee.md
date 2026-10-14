## Problem

Received a Jira service request from a new employee, Bill Smith, requesting an Active Directory account to begin working in the Finance Department.
[User requesting account in Finance Department] ([images/ticket-04/01-Jira-Request.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/ba8b7c9caf347142c86abb205dcc25a858507c3e/images/ticket-04/01-Jira-Request.png))

## Troubleshooting

Located Finance department Organizational Unit (OU) within Active Directory Users and Computers.

Created a new user account for Bill Smith using the company's naming convention, BSmith and placed the account in the Finance OU. 
[Account created] ([images/ticket-04/02-Account-Created.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/ba8b7c9caf347142c86abb205dcc25a858507c3e/images/ticket-04/02-Account-Created.png))

Assigned the appropriate permissions to allow the user access to Finance resources.

## Resolution

Successfully logged into the domain workstation using Bill Smith's account and verified that the Finance network drive was automatically mapped and accessible.
[Successful login] ([images/ticket-04/03-Successful-Login-and-Finance-Drive.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/ba8b7c9caf347142c86abb205dcc25a858507c3e/images/ticket-04/03-Successful-Login-and-Finance-Drive.png))

User confirmed they were able to log into their account, Jira ticket was resolved. 
[Jira ticket resolved] ([images/ticket-04/04-Jira-Ticket-Resolved.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/ba8b7c9caf347142c86abb205dcc25a858507c3e/images/ticket-04/04-Jira-Ticket-Resolved.png))
