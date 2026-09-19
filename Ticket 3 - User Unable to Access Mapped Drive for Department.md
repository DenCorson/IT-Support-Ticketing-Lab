Ticket 3 - User Unable to Access Mapped Drive for department

## Problem

User, Al Bundy, reports that they are unable to see their department drive mapped to their account.

[User unable to see Finance drive] ([images/ticket-03/01-finance-drive-missing.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/c963d6973daaa6ab33304fc922d828874cbcec16/images/ticket-03/01-finance-drive-missing.png))

## Troubleshooting

- Verified the Finance network share was created and accessible through '\\DC1\Finance'.
- Verified the user was a member of the appropriate Finance security groups.

[Finance share and GPO configuration] ([images/ticket-03/02-finance-share.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/abb2fff8d68a117005a310d74f5662ed464b44ea/images/ticket-03/02-finance-share.png))

- Created and linked a GPO to the Finance OU to map '\\DC1\Finance' as the T: Drive.

[Finance drive mapping GPO] ([images/ticket-03/03-drive-map-configuration.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/abb2fff8d68a117005a310d74f5662ed464b44ea/images/ticket-03/03-drive-map-configuration.png))

- Ran 'gpupdate /force' on the client workstation to refresh Group Policy.
- Used 'gpresult' to verify whether the Finance Mapped Drive GPO was being applied.
- Identified that the GPO was initially being denied due to security filtering.
- Updated GPO delegation to allow Authenticated Users Read access while keeping policy application restricted to the Finance security group.
- Refreshed Group Policy and verified that the Finance Mapped Drive GPO successfully applied.

[Finance GPO successfully applied] ([images/ticket-03/04-gpresult-success.png]([https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/abb2fff8d68a117005a310d74f5662ed464b44ea/images/ticket-03/03-drive-map-configuration.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/abb2fff8d68a117005a310d74f5662ed464b44ea/images/ticket-03/04-gpresult-success.png)))

## Resolution

The Finance Mapped Drive GPO successfully mapped '\\DC1\Finance' as  the T: drive on the user account.

The user logged back into their account, confirmed that the Finance drive was visible and accessible.

[Finance T drive successfully mapped] ([images/ticket-03/05-finance-drive-mapped.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/abb2fff8d68a117005a310d74f5662ed464b44ea/images/ticket-03/05-finance-drive-mapped.png))

User was able to login to their workstation.

Ticket was resolved and closed.

[Resolved Jira ticket] ([images/ticket-03/06-jira-resolved.png](https://github.com/DenCorson/IT-Support-Ticketing-Lab/blob/8883a836ca7225e586278c51ea8bd884c8498f5d/images/ticket-03/06-jira-resolved.png))
