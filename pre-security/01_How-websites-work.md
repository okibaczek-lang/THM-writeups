# How Websites Work — TryHackMe

## What is this room about
This room explains how websites are built 
and introduces basic security issues that 
can appear in poorly written web code.

## What I learned
- The difference between front end and back end
- HTML structures a webpage and displays 
  text and images
- JavaScript adds interactivity to a webpage
- If website code is poorly written, an attacker 
  can view sensitive data like login credentials 
  in the page source
- What HTML Injection is — when a website allows 
  user input to be displayed without filtering it, 
  an attacker can inject HTML or JavaScript code 
  and control how the page looks and behaves

## Tasks

### Showing a cat image
I had to modify an HTML element attribute 
to display a cat image. I added the .jpg 
extension to the file path to make it work.

### Building a new HTML line
I had to write a new line of HTML code 
to display a dog image. I added:

img src='img/dog-1.png'

This taught me how img tags work and how 
file paths are used in HTML.

<img width="1919" height="948" alt="image" src="https://github.com/user-attachments/assets/e783fd90-bf40-4cfc-a698-d79a0bdfb3be" />


## What was difficult
At first I wasn't sure how to spot 
vulnerabilities in website code. This room 
made it clear that bad input handling is 
one of the most common security issues 
in web applications.
