# sencha-touch-chat

Example chat application based on [Sencha Touch 2.3.1](http://www.sencha.com/products/touch/ "Sencha Touch"), [NodeJS](http://nodejs.org/ "NodeJS") and [Socket.IO](http://socket.io/ "Socket.IO").

![](https://github.com/rzen/sencha-touch-chat/blob/master/resources/Screenshots/Screenshot%20-%20Login.png?raw=true) ![](https://github.com/rzen/sencha-touch-chat/blob/master/resources/Screenshots/Screenshot%20-%20MessageList.png?raw=true)

![](https://github.com/rzen/sencha-touch-chat/blob/master/resources/Screenshots/Screenshot%20-%20node%20ChatServer.js.png?raw=true)

## Installation

### Go to your webserver's document root:

	$ cd /var/www
	(or your app folder on Desktop)

In this README.md we'll assume that the location of this folder is /var/www. Naturally it will vary (maybe app folder on Desktop).


### Clone this project from GitHub:

	$ git clone https://github.com/rzen/sencha-touch-chat.git

If you're deploying to linux server: Clone repo to your apache document root. 


### Build the application

	$ sencha app build


### Install NodeJS:

Download from http://nodejs.org/download/ and follow download and installation instructions.


### Install Socket.IO (from main repo directory):

	$ cd nodejs
	$ npm install socket.io


## Running chat server

This project uses nodejs as its chat server. Server code is located in nodejs/ChatServer.js.

To start chat server:

	$ node ChatServer.js


Go to your main directory (if you are in nodejs, "cd ../").

Now run 
	$ sencha web start

Navigate to http://localhost:1841

Chat


## Customization

This project uses http://localhost for the app itself and http://localhost:3333 as WebSocket port. This is hardcoded in the following files;

	index.html
	app.json
	app/view/Login.js
	nodejs/ChatServer.js


## Using Sencha Cmd

As is the project runs in "development mode." Which means individual classes get loaded separately. 

Using Sencha Cmd to compile project takes load time for this app from roughly 10 seconds to under 1. 

Here's how:

	$ cd /var/www
	$ sencha app build production

Packaged code will be available in

	/var/www/sencha-touch-chat/build/Chat/production


## History

Feb 2nd, 2014 Updated for Sencha Touch 2.3.1. Simplified installation. Enjoy!


## FAQ

Be the first to contribute an FAQ.


## Free to use

This demo code is free to be used for any legitimate purpose. Hopefully to learn.

Please consult with Sencha on using Sencha Touch in your projects.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

The Software shall be used for Good, not Evil.

(Thank you Douglas Crockford)


## Disclaimer

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
