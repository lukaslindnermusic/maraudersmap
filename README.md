# maraudersmap
A Harry-Potter-Marauders-Map-styled Dashboard for your homelab

_(Code will follow soon.)_

Me. Harry Potter Fan. Named my NAS "Gringotts" already. Then I bought a raspberry pi for security and monitoring tools (which I of course fittingly named Marauders Map).
After a few months, I had installed a few open source tools and quickly was in need of an overview dashboard.
What device would be good to run the dashboard? Ah yes, of course, the pi that already runs monitoring tools and therefore already "sees every other device".

So... should I install a random dashboard that's already out there? Nooooo... wait...
what was the name of the pi again?
What does the Marauders Map do?
Wouldn't it be fun if....

![01a](https://github.com/user-attachments/assets/3aba44d3-15b1-49e4-9e79-277dd024134b)

We start with the login view:

![05](https://github.com/user-attachments/assets/ee2f3fbe-6fec-4b08-94bc-1ac3e85a3726)

After a successful login, of course, the sentence "I solemnly swear that I am up to no good" appears.
Then we can see the map. It distinguishes between:
- Locations: This represents a physical location, such as your appartement or house, or a datacenter.
- Rooms: Basically for devices that host multiple applications, docker container, multiple websites etc.
- Persons: These are either services on a host (aka. inside a room) or single devices that do not host multiple services themselves

![01b](https://github.com/user-attachments/assets/b5b224ca-ea4f-4994-b0ae-dea616f1d6ad)

In the screenshot, you can see that I have a room called "Gringotts" for my main NAS.
For example, the NAS runs a Jellyfin Media Server, which on the map is represented by a person standing inside of that room.

You can choose from different Designs for the locations and rooms. The persons are animated, so they will walk around a little bit every once in a while
(unless you deactivate that feature for a specific person or if the person is offline).

Also, you can see that I have multiple locations. The big one on the left is my home network. Bottom right is a family members house, where I store my offsite backups on a second NAS called "Bunker".
The one in the top right (it is actually a room... you can select "Empty" as Design for a Location) represents my VPS that hosts my website.


If a person is offline, you can decide to either reduce the opacity, show the person with a red warning, hide the person completely or leave it as is.
For a room, you additionally have the option to let it become a "Wall" in case its offline (of course you can also add constant "walls").
I use this feature with the "Peeves" wall in the screenshot. This actually is a raspberry pi zero 2 w that only runs motion eye with a security camera.
I only turn it on when I want to monitor my home while I am away, so if it is offline, I don't need to see an empty room on my marauders map dashboard.
(Oh, that security camera raspberry pi of course is called "Revelio".)

When you click on a Peson or Room Label, you get details about that service/device:

<img width="1828" alt="02" src="https://github.com/user-attachments/assets/282f8be6-fde8-47e9-8a1c-da2e96fac870" />

Every room or person has a title, subtitle and you can choose from a list of icons. You can connect your Uptime Kuma Instance, which allows you to specify an UptimeKuma Monitor for each person and room. As a fallback (or if you don't want to use Uptime Kuma for uptime monitoring) you can also utilize nmap scans. Of course, both options are optional and you can use the map also to just statically show everything.

You can assign IPs and URLs to each device (person/room), which are shown in a list in the details view.

Every room, person or link can get tagged. With tags, you can filter your dashboard:

![03](https://github.com/user-attachments/assets/474631ee-5eb8-4da4-a106-73cb2fc9e3d0)

In the settings, you can add, edit or remove locations, rooms, persons, tags or users (yes, there is multiple user support).
Also, you can set up your Uptime Kuma and nmap integrations, your map preferences, you can remember your session (so that you stay logged in) or you can change your password.

<img width="1828" alt="04" src="https://github.com/user-attachments/assets/0a7b5b3b-9dab-45d7-bfeb-87108783dba7" />

You can position the locations on the entire map, and you can position the rooms in their assigned locations on a grid system:

<img width="1828" alt="07" src="https://github.com/user-attachments/assets/a46ead78-2cd8-49f0-a41a-f57ef2b0f0df" />

This is the view to add links to a person or room:

<img width="1828" alt="08" src="https://github.com/user-attachments/assets/aca84372-550d-4b87-8821-6e9a11494055" />

You can create mutliple users and decide, which user can see what locations, rooms, persons and links:

![09](https://github.com/user-attachments/assets/699e5684-a09d-4155-a205-f5d39397c4b8)


And, yeah... that's it. 
Coded with PHP + SQLite Database, Javascript, HTML+CSS.




