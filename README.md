# Usage

This extension is a bit different from the old AddOrUpdate from EF (not Core). You will have to pass the object (or list of objects) with a ref. Also, you will have to send a dynamic object specifying the fields you'll be using to check if EF will add a new one up update an existant object.

Single object:
``` c#
context.Users.AddOrUpdate(ref singleUser, x => new { x.SocialSecurityNumber })
```
List of objects:
``` c#
context.Users.AddOrUpdate(ref listOfUsers, x => new { x.SocialSecurityNumber })
```
