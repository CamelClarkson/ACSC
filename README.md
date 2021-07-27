# ACSC 2021
The Advanced Cyber Security Camp provides students with a thorough introduction to different types of malware and attacks.
Students will learn about different attack vectors and implement there own attack vectors along with how to mitigate them.
The target demographic are students in years 9-12 of schooling who have taken either a first year programming course or introductory Cyber Security Camp offered by the instructors.

## Goals
- Understanding of different types of attacks **list them out once the course is finished**
- Being able to think critically about software development from a security focus

## Day 1: Introduction
### Introduction
- Instructos: Dr. Chen Liu and Mr. Zander Blasingame
- Students:
  - Name
  - Year
  - School
  - Why did you choose this course
  - What is your anticipated field of study

### Linux Overview


### Additional Setup for Windows Users
- Install the free home edition of [MobaXterm](https://mobaxterm.mobatek.net/download.html)
- Create an SSH session

### Connect to the Server
- IP address is `3.12.96.179`
- Account usernames are given by `<fistletter><lastname>`
- The default password is `password`
- Use the ssh command to connect to the server
- Use the command `passwd` to change your password upon login

### Review Linux Permissions


## Day 2: XSS
- Cross site scripting attack: [video](https://www.youtube.com/watch?v=zv0kZKC6GAM)
- Create a new directory for this project and navigate to it
- Download `public.tar.gz` from this github repo
- Use the `tar` command to extract the conents and use the `man` command to figure out what flags to use
- The contents of the `public.tar.gz` file contain all the HTML, CSS, and client-side JS for you website
- The main html file is located at `public/index.html`
- Install the express package with `npm install express`
- Create `app.js` in your project directory
- Add the following code to your `app.js` file
```js
// Import express package
var express = require('express');
var app = express();
// specify port number
var port = 8000;

// Handle request to serve main file
app.get('/', function(req, res) {
        // __dirname is the working directory of the project
        res.sendFile(__dirname + '/public/index.html');
});

// allow the server to serve content from public directory
app.use(express.static('public'));

// Set server to listen to `port`
app.listen(port, function() {
        console.log('Server on port: ' + port);
});
```
- Change the port number to one the instructors will give you
- Run the server in the background using the command `node app.js &`
- To see your webpage, open up your preferred web browser and navigate to `http://3.12.96.179:<your-port-number-here>`
- Ensure that you see your web page
- Kill the node server using `kill`



## Day 3: Encryption (Introduction)

## Day 4: Encryption (RSA Key Generation)

## Day 5: Ransomware

Work through this as a class [link](https://github.com/jimmy-ly00/Ransomware-PoC)
