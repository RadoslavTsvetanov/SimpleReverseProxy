# SimpleReverseProxy

# Why
- I needed a https reverse proxy with more complex filtering functionality and nginx and traefik weren't good enough
- to learn a new language I wanted to learn for a long time
- for funnies
- I needed to write tests for my redirecting logic and writing them in a real lang would have made it easier

# Features 

## Middlewares 
there is a folder called middlewaresin which every file is executed as middleware, for now only the tool lang is supported buy in the future there will be support for different langs which will be run inside a sandbox env

## Handlers
in the handlers folder again you make a handwr for redirecting logic
which should follow this function signature
```
fn handler(req: Req) -> string | null
```
where the return is the redirect url and if it is null we invoke the nest handleramd like that until one returns a string

also handles are executed in order e.g. First fails we ge the second etc....
## easy to set up

## easy to set up ssl certs
