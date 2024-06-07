# Blazor Puzzle #36

## Can't Log Out!

YouTube Video: https://youtu.be/RdPp2CgUz9Y

Blazor Puzzle Home Page: https://blazorpuzzle.com

### The Challenge:

With the latest templates for Blazor adding authentication and authorization is something that requires you to copy in pages and features from another template. In this example, I've started with the base Blazor application template and copied in all of the pages and content from the account folder in another template that had authentication enabled.

I'm able to register as a new user, login as that user and interact with the website. Problem is I can't log out as this user. Attempt to log out I get a 404 error screen

What's the problem with my project?

### The Solution:

The project is missing a critical line of code at the bottom of the *Program.cs* file before `app.Run();`

```c#
app.MapAdditionalIdentityEndpoints();
```

