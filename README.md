# How to run the project

## Requirements:
 - git
 - docker (https://docs.docker.com/engine/install/ubuntu/)
 - docker compose (https://docs.docker.com/engine/install/ubuntu/)
 - meta (optional) `npm i -g meta`
 - meta-git (optional) `npm i -g meta-git`
 - make (optional) `sudo apt-get -y install make`

## Steps: 
 1. Clone the repositories:
    - Recommended: clone the repos with the `meta-git` cli
    
     ```bash
     meta git clone https://github.com/marnec/dynamic-categories
     ```
    - Alternatively: clone the three repos and reproduce the follwing folder structure:
      - dynamic-categories (git@github.com:marnec/dynamic-categories.git)
        - frontend (git@github.com:marnec/dynamic-categories-frontend.git)
        - backend (git@github.com:marnec/dynamic-categories-backend.git)


2. Start the project:
    - If you have `make` installed: `make start`
    - Otherwise `docker compose --env-file dev.env up`
    - First startup may take a while since db migrations will create and populate tables

3. Visit:
   - `http://localhost:4200` for UI
   - `http://localhost:3000` for REST API
   - `http://localhost:3000/doc` for Swagger UI