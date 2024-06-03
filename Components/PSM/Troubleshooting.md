---
layout: default
title: Troubleshooting
parent: PSM
---
# Troubleshooting

### Error - User Can't Connect

- Check if the account being used is in compliance.
- Check if the account is locked in AD.
- See if the user has the right access.
- Check Trace logs.

### Error – Request Timed Out

- The issue pertains to the access to the endpoint -> Contact Application team / AD.

### Error – Entire Environment Cannot Connect

- Check predefined user as it may be locked. As the entire environment cannot connect.

### Shadow User - Created When the User Connects

- Holding up connection.
- Delete Shadow user from browser history.
- Connect again; it will create a new shadow user, and you will be able to connect.

### Load Balance

- The configuration on the load balancer is incorrect.
- Use a standalone PSM to connect. If it works, contact the F5 team and have them fix the load balance.
