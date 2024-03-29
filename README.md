# Abungo

Simple chat app made with node.js and Socket.IO.

## Simple and anonymous

The server doesn't store any information about the users or keep logs. It simply relays the data from one client to the rest. Users can chat privately in chat rooms. The default room is "yeya".

## Responsive layout

The Abungo client is minimally designed and adapts to different screen sizes.

![Abungo on a PC](http://i.imgur.com/uHIjlEu.png)

![Abungo on a smartphone](http://i.imgur.com/BzgCj67.png)

## Admin dashboard

Abungo comes with a simple command-based admin dashboard for chat moderation. It can be accessed at `http://localhost:3000/admin` and looks like this:

![Abungo Admin Dashboard screenshot](http://i.imgur.com/zEb8OxJ.png)

Commands you can use:

+ `say <text>` - send a chat message globally (all rooms can see it)
+ `list` - lists all users
+ `brainwash` - clear users' screens
+ `disconall` - disconnect all users
+ `kick <room>:<nick>` - force a user to disconnect
+ `stop` - stop the server

A password is required to access the admin dashboard. By default, the password is `default` and it can be changed by making an `adminpassword` file containing the new password in the Abungo directory. 

```bash
# the simplest way to do it

printf "my_super_secure_password" > adminpassword
```

**It is not recommended to use the same password as your other accounts since Abungo is not encrypted**.

## Running Abungo

First, you'll need to download and install [node.js](http://nodejs.org) if you haven't already.

`cd` to the Abungo directory and install Socket.IO, Express and body-parser:

```bash
npm install socket.io
npm install express
npm install body-parser
```

After you have everything installed, run `node server` from the Abungo directory. Navigate to `http://localhost:3000` in your browser to see it in action.

You might also want to check it out live at https://abungo.jit.su
