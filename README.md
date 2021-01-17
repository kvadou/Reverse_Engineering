<h1 align="center">Unit 14 Sequelize: Reverse Engineering Code</h1>

## Reverse_Engineering

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Explanation](#explanation)
- [Contributing](#contributing)
- [Questions](#questions)

## Description

The assignment was to walk through a code base that was provided to me and write a tutorial explaining every file and its purpose.

## Installation

`create MySQL db named "passport_demo`

`modify config.json with your username/password`

`run "npm i" from command line`

`run "node server" from command line`

`open "http://localhost:8080" in your browser`

## Usage

AS A user that wants to securely log into a website

I WANT to make sure that my username and password stored

SO THAT I don't need to worry about using a website

## Explanation

Develop

    => config

        => middleware

            => isAuthenticated.js {This helps us restrict routes a user is allowed to visit if they are not logged in}

        => config.json {This allows us to connect to the database and server with our MySQL login credentials}

        => passport.js {JavaScript logic that tells passport we want to login with a email address and password}

    => models

        => index.js {Connects us to the database and imports users log in data}

        => user.js {Uses bcryptjs for password encryption, makes the database more secure.  Forces user the enter a valid email address, and does not allow the password field to be left empty}

    => public

    => routes

        => api-routes.js {Contains routes for signing up a user, logging out a user and getting users specific data to be displayed client side}

        => html-routes.js {Routes that check whether user is signed in, whether user already has account etc and sends them tio the member page.  If user is not signed in, they are routed to the sign-up page}

    => package.json {Contains all package info, node modules used, version info}

    => server.js {Requires our npm packages, establish our PORT number, creates express and middleware, creates routes and syncs database & logs message in terminal on successful connection to server}

## Contributing

:octocat: [Doug Kvamme](https://github.com/kvadou)

## Questions

Contact me with any questions: [email](mailto:dougkvamme@gmail.com) , [GitHub](https://github.com/kvadou)<br />
