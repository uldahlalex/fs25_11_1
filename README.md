This project spans weeks 9 and 10 and concludes all websocket work.

![alt text](image-1.png)

#### Remote repo on Github: `https://github.com/uldahlalex/fs25_kahoot` 

### Agenda, Wednesday 26th of February (week 9)
- 08:15: Presentation: Project reveeal: **The Kahoot Clone** & Relevant theory
    - Presentation link: `https://docs.google.com/presentation/d/1Fjfp4FHT1ZtFiEs_8sQa-VAXPOTbuQE6pqkBbDV2aG8/edit?usp=sharing`

### Agenda, 🎂Friday 28th of February🎂 (week 9)
- 08:15: Presentation
    - Deployment of WebSocket APIs
    - Unit testing with real networking
    - NSwag TS generator
- 09:00: One of two of you will help me pick up and carry cake from Højvangs bakery next to the school
- 09:15: We eat cake and program awesome kahoot clone


*Week 10 do not have any presentations*

# The Kahoot Clone Assignment

## Features

The following Kahoot-like features must be implemented:
- When arriving on the "landing page", clients are added to a lobby
- When the admin "starts" a game, all the clients in the lobby are added to the game-room
- Questions are broadcasted by the admin to all clients in the gameroom (beginning of a new "round").
    - Players send ansers to the server during the question phase of the round.
    - After a certain time-delay, the "results" of the round is broadcasted by the server, and the question phase is over.
    - The answers are displayed in the "results" phase.


## Implementation details

- Data should be saved.
    - You must store peristed data in a relational database (like this one `https://aiven.io/free-postgresql-database`).
    - Temporary WebSocket state can be stored in ConcurrentDictionaries


## Tips

- You may build you own "ConnectionManager" from scratch or use a generalized solution I have here: `https://gist.github.com/uldahlalex/a75d4dc99c3cfb99b15a8db4a4af90ba` which can be used for a lot of different business cases including this one.
- You may build your own database schema from scratch or use the one I used in my demo: `https://gist.github.com/uldahlalex/dedc2736839d4f72a5f09aa1c5f6d1d0`
    - The ID's are all text (with no fancy auto-generate, so I recommend you just make GUID's in C# and cast .ToString() before saving)

## Release party

When the project is finished, we will have project showcases.
- Each group will host a kahoot quiz live in the classroom - where everyone else will be playing along (yes this means deployment)
- The date for the release party will be Wednesday 12th. Just after the presentations we will begin the next major topic in Fullstack 2025 (same day).