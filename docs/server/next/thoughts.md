# Thoughts on Next.js

## Purpose

It seems to be a web framework intended for sever-side rendering of react components.

## Problems

I haven't done too much with it yet, but from what I can see everything is done server-side.  
As far as I can tell, there is no ability for the client to send ajax requests to the server.  
This looks to me like an issue for usability since it would probably be faster to get data from the server than to render and entire page and send it instead.  

## Benefits

The good side that I can see from this is for static site generation. It would be easy to create a static site from data on a database and deploy to production on S3 or something.  