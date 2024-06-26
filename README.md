# SNAKE NETWORK GAME

## Overview

This project is currently in the development stage and features a multi-player Snake game. 

The server backend is implemented in Go, utilizing socket syscalls for efficient network communication. 
The client-side interface and the game logic are developed in Python, providing a smooth and interactive gaming experience.

### Key Features

- **Server:** Written in Golang, the server harnesses the power of low-level socket syscalls to manage real-time multiplayer game states efficiently.
- **Client and Game Logic:** Both are crafted in Python, designed to offer intuitive gameplay and dynamic interaction between users.


## Pre-requisites:
- Install Docker and Docker Compose

## Setup Instructions:
1. Clone this repo to you local machine.
2. `cd` into the project directory.
3. Edit `docker-compose.yml` to specify the number of client and server instances you need. --> ( by default: 2 clients and 1 game server).
4. Run the following to start your containers in the background: 
	- Run docker-compose to start containers in background ```docker-compose up -d```
5. Start terminal sessions into running containers:

   *Server:*
   - For the server: `docker exec -it snake_network_game-server-1 /bin/bash`
   
   *Clients:*
   - For the 1st client: `docker exec -it snake_network_game-client-1 /bin/bash`
   - For the 2nd client: `docker exec -it snake_network_game-client-2 /bin/bash`
   - For the nth client: `docker exec -it snake_network_game-client-n /bin/bash`

6. Once you have a terminal session:
   - In the server container, run: `cd server/cmd/` and then `go run server.go`
   - In client containers, run: `python3 snake.py`

7. To stop all containers use:
   ```docker-compose down```

## Default Settings:
- By default, the server is configured to handle 3 players.
- Default usernames and passwords for each player:
  - **Player 1:**
    - Username: `user1`
    - Password: `password1`
  - **Player 2:**
    - Username: `user2`
    - Password: `password2`
  - **Player 3:**
    - Username: `user3`
    - Password: `password3`


  
