# github-visualisation

To run this project simply donwload the repository, un-zip it, and then double click the index.html file to open it within your browser.
From there simply enter a valid username and various statistics will be presented to you. The first bar chart represents all the languages
that your repos use, and the percentage of usage each language sees in total.

The second bar chart displays how many commits you have made on GitHub per month for a year, with the option to change the year. This bar
chart may take a few seconds to load, depending on how many repositories and commits a user has.

The NodeJS server is not meant to be run on your local machine, and the 'Get All Info' button doesn't work anywhere except on my own webserver
@ https://github-api-access.darragh.io

The reason the NodeJS server is being used on my own webserver is to allow the functionality of the 'Get All Info' button, which ascertains information which is not publically
available, by communicating with GitHub and allowing a user to sign in to obtain a temporary access token which allows my web application to see all of the public and private
repositories. The NodeJS server is required as a bypass to a common browser security precaution which prevents GitHub from sending a user token to my webpage. My web application
sends a 'code' to the NodeJS server, the NodeJS server sends this code to GitHub and receives an access token, and then the NodeJS server sends the access token back to my webserver,
thus bypassing what is known as a CORS (Cross Origin Remote Sharing) violation that occurs when a abrowser requests a token from GitHub. (A problem on GIthub's end, they don't have the
necessary http headers set to allow browsers to receive access tokens)

As previously mentioned, a running and fully functional version of this web application is running @ https://github-access.darragh.io/
