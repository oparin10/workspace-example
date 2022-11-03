# Repository structure

This is an overview and a set of guidelines of how this repository is structured and how one should operate within it

## Main folders

- ./client
- ./server

There are 2 main workspaces folders; the client (hosts client-side applications (frontend)) and the server (Cargo workspace hosting server-side related services written in Rust)

## Workspaces

The 2 main workspaces are orchestrated using pnpm workspace feature (for client-side code) and the Cargo workspace feature (for server-side code)

## Commands

Preferably, commands should be always run from the root of the repository, leveraging pnpm and Cargo workspace features to filter a command to an specific package(s).

## Other types of files

Docker files, configuration files, deployment related config and such should live in the root of the repository

## Known issues

### PNPM workspace and Storybook

Storybook doesn't work well with pnpm global store symlinking strategy, so a .npmrc file containing a public hosting pattern for all Storybook related packages (storybook, react and babel) has to exist so it actually works
