# magus-landing

## Purpose
Static landing page for sirazad.com.
No JavaScript framework, no build step.
Plain HTML + CSS served by nginx alpine.

## Stack
- HTML + CSS only
- nginx:alpine as server (ARM64 compatible)
- Deployed as a Docker container via sirazad-platform

## How it runs
This repo is NOT deployed standalone.
The platform repo (magus-platform) builds and runs this as a service.
docker-compose.yml lives in ../platform/, not here.

## Design
- Dark theme, fantasy RPG aesthetic to match the inventory app
- Clean and minimal
- Each service gets a card/link when added

## Current services
- Inventory → https://inventory.sirazad.com

## Adding a new service
Add a new link/card to index.html.
Commit and push.
On server: cd /home/deploy/platform && docker compose up -d --build landing

## File structure
landing/
├── index.html
├── nginx.conf
├── Dockerfile
└── CLAUDE.md
