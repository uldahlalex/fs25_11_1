#### Remote repo on Github: `https://github.com/uldahlalex/fs25_11_1` 

### Agenda, Wednesday, 12th of February
- 08:15: Presentation of Kahoot Guided Solution (+ optional student implementations)
- 08:45: Short break
- 09:00: Introduction to Onion Architecture

### Notice: The format has recently been changed: Now I do a walkthrough of how to solve the exercise + you will have chance to share your solutions / implementation proposals

___

### Onion Exercise: Setting up the layers (exercise starting  9:30 o'clock)

![alt text][logo]

[logo]: image.png
<style>
  img[alt="alt text"] {width: 200px;}
</style>

Construct an onion-style .NET backend with the following projects in a single solution (with a single API for now):

- Startup
- API.REST
- Application
- Infrastructure
- Core/Domain

There are different onion architecture flavors, but I recommend applying the following rules:

- The Core/Domain has no references to any other project, but any project can know about it.
- The Application project can reference Core/Domain + 3rd party libraries(nugets), but no other .csproj in the solution.
- The infrastructure only knows about Application and it's dependencies. *(Some onion style architectures prefer to have only infrastructure reference to core/domain - especially in older literature)*
- All API projects know about Application and its dependencies.
- The startup can know about any project and exists to perform dependency injection (and some small utilities like provide living documentation, starting the program, etc)

I have made an application here using fullstack 2025 technologies with onion architecture. It will be a reference application used ocasionally in examples: `https://github.com/uldahlalex/fullstack2025`

Once you have set up the onion, try and build some basic CRUD functionality with a single entity.

## Examples of exam questions regarding onion architecture

**Q: How can the application layer make use of infrastructure objects when there is no direct project reference to the infrastructue layer from application layer?**

**Q: Why is it relevant to have a separate "Startup" project instead of simply starting the program using the API?**

