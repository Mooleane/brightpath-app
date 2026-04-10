# BrightPath

## Project Overview 
BrightPath is an app designed to connect students to the tutors of their choice on the subjects they want covered, solving the problem of students not connecting to their material because of different teaching styles from different tutors.

## Quick Start 
```bash
docker build -t brightpath-app . 
docker run -p 3000:3000 brightpath-app
```

## Architecture 
BrightPath is a two-stage Docker build.

It uses node:20-alpine to install the dependencies used to create the app in the Build Stage.

Then it uses node:20-alpine to copy the completed build files, to then run the production server.

This keeps the final image efficient by only using the finished files used within the app.

## Business Value 
Docker makes sure that BrightPath runs the same on any type of operating system, whether that be Windows, MacOS, Linux, etc. This fixes the "works on my machine" problem by making the app reliable for both students and tutors regardless of the device they use.

## Tech Stack
- Next.js
- React
- Node.js
- Docker
- Tailwind CSS
- ESLint